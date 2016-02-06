# com-chilipeppr-widget-xyz
The Axes widget shows the XYZA values of the axes of your CNC controller. It also enables you to jog, home, change units, and change Work Coordinate Systems.

![alt text](screenshot.png "Screenshot")

## ChiliPeppr Widget / XYZ Axes

All ChiliPeppr widgets/elements are defined using cpdefine() which is a method
that mimics require.js. Each defined object must have a unique ID so it does
not conflict with other ChiliPeppr widgets.

| Item                  | Value           |
| -------------         | ------------- | 
| ID                    | com-chilipeppr-widget-xyz |
| Name                  | Widget / XYZ Axes |
| Description           | The Axes widget shows the XYZA values of the axes of your CNC controller. It also enables you to jog, home, change units, and change Work Coordinate Systems. |
| chilipeppr.load() URL | http://raw.githubusercontent.com/chilipeppr/widget-axes/master/auto-generated-widget.html |
| Edit URL              | http://ide.c9.io/chilipeppr/widget-axes |
| Github URL            | http://github.com/chilipeppr/widget-axes |
| Test URL              | https://preview.c9users.io/chilipeppr/widget-axes/widget.html |

## Example Code for chilipeppr.load() Statement

You can use the code below as a starting point for instantiating this widget 
inside a workspace or from another widget. The key is that you need to load 
your widget inlined into a div so the DOM can parse your HTML, CSS, and 
Javascript. Then you use cprequire() to find your widget's Javascript and get 
back the instance of it.

```javascript
// Inject new div to contain widget or use an existing div with an ID
$("body").append('<' + 'div id="myDivWidgetXyz"><' + '/div>');

chilipeppr.load(
  "#myDivWidgetXyz",
  "http://raw.githubusercontent.com/chilipeppr/widget-axes/master/auto-generated-widget.html",
  function() {
    // Callback after widget loaded into #myDivWidgetXyz
    // Now use require.js to get reference to instantiated widget
    cprequire(
      ["inline:com-chilipeppr-widget-xyz"], // the id you gave your widget
      function(myObjWidgetXyz) {
        // Callback that is passed reference to the newly loaded widget
        console.log("Widget / XYZ Axes just got loaded.", myObjWidgetXyz);
        myObjWidgetXyz.init();
      }
    );
  }
);

```

## Publish

This widget/element publishes the following signals. These signals are owned by this widget/element and are published to all objects inside the ChiliPeppr environment that listen to them via the 
chilipeppr.subscribe(signal, callback) method. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-pub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Subscribe

This widget/element subscribes to the following signals. These signals are owned by this widget/element. Other objects inside the ChiliPeppr environment can publish to these signals via the chilipeppr.publish(signal, data) method. 
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-sub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Foreign Publish

This widget/element publishes to the following signals that are owned by other objects. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignpub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-widget-serialport/send</td><td>We publish to the serial port Gcode jog commands</td></tr>    
      </tbody>
  </table>

## Foreign Subscribe

This widget/element publishes to the following signals that are owned by other objects.
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignsub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-interface-cnccontroller/axes</td><td>We want X,Y,Z,A,MX,MY,MZ,MA axis updates.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-interface-cnccontroller/coords</td><td>Track which is active: G54, G55, etc.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-interface-cnccontroller/plannerpause</td><td>We need to know when to pause sending jog cmds.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-interface-cnccontroller/plannerresume</td><td>We need to know when to resume jog cmds.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-interface-cnccontroller/units</td><td>Deprecated. Not listening to this anymore. See next.</td></tr><tr valign="top"><td>/com-chilipeppr-widget-xyz/com-chilipeppr-widget-3dviewer/unitsChanged</td><td>Listenting to see if the 3D Viewer is telling us that the user Gcode is in a specific coordinate and then just assuming we will only be sent axes coordinate updates in that unit. Not using /com-chilipeppr-interface-cnccontroller/units anymore.</td></tr>    
      </tbody>
  </table>

## Methods / Properties

The table below shows, in order, the methods and properties inside the widget/element.

  <table id="com-chilipeppr-elem-methodsprops" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Method / Property</th>
              <th>Type</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>id</td><td>string</td><td>"com-chilipeppr-widget-xyz"</td></tr><tr valign="top"><td>url</td><td>string</td><td>"http://raw.githubusercontent.com/chilipeppr/widget-axes/master/auto-generated-widget.html"</td></tr><tr valign="top"><td>fiddleurl</td><td>string</td><td>"http://ide.c9.io/chilipeppr/widget-axes"</td></tr><tr valign="top"><td>githuburl</td><td>string</td><td>"http://github.com/chilipeppr/widget-axes"</td></tr><tr valign="top"><td>testurl</td><td>string</td><td>"http://widget-axes-chilipeppr.c9users.io/widget.html"</td></tr><tr valign="top"><td>name</td><td>string</td><td>"Widget / XYZ Axes"</td></tr><tr valign="top"><td>desc</td><td>string</td><td>"The Axes widget shows the XYZA values of the axes of your CNC controller. It also enables you to jog, home, change units, and change Work Coordinate Systems."</td></tr><tr valign="top"><td>publish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>subscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignPublish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignSubscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>init</td><td>function</td><td>function () </td></tr><tr valign="top"><td>pencilSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>pencilOnMouseover</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>pencilOnMouseout</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>pencilClick</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>pencilCtr</td><td>number</td><td></td></tr><tr valign="top"><td>pencilKeypress</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>pencilHide</td><td>function</td><td>function (tgtEl) </td></tr><tr valign="top"><td>initAs3dPrinting</td><td>function</td><td>function () </td></tr><tr valign="top"><td>setupShowHideWcsBtn</td><td>function</td><td>function () </td></tr><tr valign="top"><td>toggleWcs</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>setupShowHideTouchBtn</td><td>function</td><td>function () </td></tr><tr valign="top"><td>showHideTouchBtn</td><td>function</td><td>function () </td></tr><tr valign="top"><td>canvas</td><td>object</td><td></td></tr><tr valign="top"><td>el</td><td>object</td><td></td></tr><tr valign="top"><td>ctx</td><td>object</td><td></td></tr><tr valign="top"><td>setupTouchArea</td><td>function</td><td>function () </td></tr><tr valign="top"><td>toggleTouchJog</td><td>function</td><td>function () </td></tr><tr valign="top"><td>canvasResize</td><td>function</td><td>function () </td></tr><tr valign="top"><td>drawText</td><td>function</td><td>function () </td></tr><tr valign="top"><td>isMouseDown</td><td>boolean</td><td></td></tr><tr valign="top"><td>mouseLastOffset</td><td>object</td><td></td></tr><tr valign="top"><td>onMouseDown</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>onMouseMove</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>onMouseUp</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>scrollPrev</td><td>object</td><td></td></tr><tr valign="top"><td>scrollFadeTimer</td><td>object</td><td></td></tr><tr valign="top"><td>scrollLastPosDir</td><td>string</td><td>"up"</td></tr><tr valign="top"><td>onScroll</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>ongoingTouches</td><td>object</td><td></td></tr><tr valign="top"><td>start</td><td>object</td><td></td></tr><tr valign="top"><td>inZMode</td><td>boolean</td><td></td></tr><tr valign="top"><td>handleStart</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>sendCtr</td><td>number</td><td></td></tr><tr valign="top"><td>sendMove</td><td>function</td><td>function (touchid, prevpos, newpos) </td></tr><tr valign="top"><td>sendDone</td><td>function</td><td>function () </td></tr><tr valign="top"><td>sendMoveZ</td><td>function</td><td>function (touchid, prevpos, newpos) </td></tr><tr valign="top"><td>handleMove</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>handleEnd</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>handleCancel</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>colorForTouch</td><td>function</td><td>function (touch) </td></tr><tr valign="top"><td>copyTouch</td><td>function</td><td>function (touch) </td></tr><tr valign="top"><td>ongoingTouchIndexById</td><td>function</td><td>function (idToFind) </td></tr><tr valign="top"><td>log</td><td>function</td><td>function (msg) </td></tr><tr valign="top"><td>findPos</td><td>function</td><td>function (obj) </td></tr><tr valign="top"><td>lastImage</td><td>object</td><td></td></tr><tr valign="top"><td>fadeCanvas</td><td>function</td><td>function () </td></tr><tr valign="top"><td>fadeCtr</td><td>number</td><td></td></tr><tr valign="top"><td>fadeCanvasStep</td><td>function</td><td>function () </td></tr><tr valign="top"><td>drawCircle</td><td>function</td><td>function (ctx, e) </td></tr><tr valign="top"><td>toolbarSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>bodyShowSmall</td><td>function</td><td>function () </td></tr><tr valign="top"><td>bodyShowNormal</td><td>function</td><td>function () </td></tr><tr valign="top"><td>options</td><td>object</td><td></td></tr><tr valign="top"><td>setupUiFromCookie</td><td>function</td><td>function () </td></tr><tr valign="top"><td>saveOptionsCookie</td><td>function</td><td>function () </td></tr><tr valign="top"><td>pauseBtnIcon</td><td>object</td><td></td></tr><tr valign="top"><td>isPausedByPlanner</td><td>boolean</td><td></td></tr><tr valign="top"><td>onPlannerPause</td><td>function</td><td>function () </td></tr><tr valign="top"><td>onPlannerResume</td><td>function</td><td>function () </td></tr><tr valign="top"><td>toggleInMm</td><td>function</td><td>function () </td></tr><tr valign="top"><td>currentUnits</td><td>object</td><td></td></tr><tr valign="top"><td>updateUnitsFromStatus</td><td>function</td><td>function (units) </td></tr><tr valign="top"><td>lastCoords</td><td>object</td><td></td></tr><tr valign="top"><td>onCoordsUpdate</td><td>function</td><td>function (coords) </td></tr><tr valign="top"><td>axisx</td><td>object</td><td></td></tr><tr valign="top"><td>axisy</td><td>object</td><td></td></tr><tr valign="top"><td>axisz</td><td>object</td><td></td></tr><tr valign="top"><td>axisa</td><td>object</td><td></td></tr><tr valign="top"><td>axes</td><td>object</td><td></td></tr><tr valign="top"><td>axismx</td><td>object</td><td></td></tr><tr valign="top"><td>axismy</td><td>object</td><td></td></tr><tr valign="top"><td>axismz</td><td>object</td><td></td></tr><tr valign="top"><td>axisma</td><td>object</td><td></td></tr><tr valign="top"><td>setupAxes</td><td>function</td><td>function () </td></tr><tr valign="top"><td>updateAxesFromStatus</td><td>function</td><td>function (axes) </td></tr><tr valign="top"><td>lastVal</td><td>object</td><td></td></tr><tr valign="top"><td>updateAxis</td><td>function</td><td>function (axis, val) </td></tr><tr valign="top"><td>menuSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>publishSend</td><td>function</td><td>function (gcode) </td></tr><tr valign="top"><td>gotoZeroM</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>gotoZero</td><td>function</td><td>function (evt, m) </td></tr><tr valign="top"><td>zeroOutAxisG10</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>zeroOutAxisG28</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>zeroOutAxisG92</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>unzeroOutAxisG92</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>homeAxis</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>isAAxisShowing</td><td>boolean</td><td></td></tr><tr valign="top"><td>showHideAxisA</td><td>function</td><td>function () </td></tr><tr valign="top"><td>ismDROShowing</td><td>boolean</td><td></td></tr><tr valign="top"><td>showHidemDRO</td><td>function</td><td>function () </td></tr><tr valign="top"><td>btnSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogFocusIndicate</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogFocusUnindicate</td><td>function</td><td>function () </td></tr><tr valign="top"><td>isInCustomMenu</td><td>boolean</td><td></td></tr><tr valign="top"><td>customMenuSetVal</td><td>function</td><td>function (itemNum) </td></tr><tr valign="top"><td>jogSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogBtn</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>baseval</td><td>number</td><td></td></tr><tr valign="top"><td>accelBaseval</td><td>number</td><td></td></tr><tr valign="top"><td>customOrigVal</td><td>object</td><td></td></tr><tr valign="top"><td>accelBaseValHilite</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>accelBaseValUnhilite</td><td>function</td><td>function () </td></tr><tr valign="top"><td>changeBaseVal</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>jog</td><td>function</td><td>function (direction, isFast, is100xFast, is1000xFast, is10000xFast) </td></tr><tr valign="top"><td>initBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>toggleBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>showBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>hideBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>forkSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>round</td><td>function</td><td>function (num, places) </td></tr>
      </tbody>
  </table>


## About ChiliPeppr

[ChiliPeppr](http://chilipeppr.com) is a hardware fiddle, meaning it is a 
website that lets you easily
create a workspace to fiddle with your hardware from software. ChiliPeppr provides
a [Serial Port JSON Server](https://github.com/johnlauer/serial-port-json-server) 
that you run locally on your computer, or remotely on another computer, to connect to 
the serial port of your hardware like an Arduino or other microcontroller.

You then create a workspace at ChiliPeppr.com that connects to your hardware 
by starting from scratch or forking somebody else's
workspace that is close to what you are after. Then you write widgets in
Javascript that interact with your hardware by forking the base template 
widget or forking another widget that
is similar to what you are trying to build.

ChiliPeppr is massively capable such that the workspaces for 
[TinyG](http://chilipeppr.com/tinyg) and [Grbl](http://chilipeppr.com/grbl) CNC 
controllers have become full-fledged CNC machine management software used by
tens of thousands.

ChiliPeppr has inspired many people in the hardware/software world to use the
browser and Javascript as the foundation for interacting with hardware. The
Arduino team in Italy caught wind of ChiliPeppr and now
ChiliPeppr's Serial Port JSON Server is the basis for the 
[Arduino's new web IDE](https://create.arduino.cc/). If the Arduino team is excited about building on top
of ChiliPeppr, what
will you build on top of it?

