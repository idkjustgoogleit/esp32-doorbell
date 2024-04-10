<h1>ESP32 S3 Doorbell via ESPHome & HA</h1>
<p align="center">
  <img src="https://raw.githubusercontent.com/idkjustgoogleit/esp32-doorbell/main/esp32-s3-doorbell/images/front-assembled.jpg" width="350" title="hover text">
</p>
<p>Couldn't find a generic DIY Doorbell with a nice angle, modular and easy to print; so made myself (another) one.&nbsp;</p>
<p>This is an updated version which I made before but didn't have IR Night-vision, and was not so stable for 24/7 video streaming because of an overheating camera module (should have used a heatsink on that one too):</p>
<p>
  <a href="https://www.printables.com/model/667022-esp32-doorbell-and-weatherstation" target="_blank" rel="ugc">https://www.printables.com/model/667022-esp32-doorbell-and-weatherstation</a>&nbsp;
</p>
<p>Like the other design, this is also not waterproof so I put a rubber band in between, because why not. There is a smoll roof included in the design just to be safe I guess.</p>
<p>Print with PETG because I don't know how direct sunlight would affect PLA.</p>
<p>
  <strong>Parts &amp; Requirements list:</strong>
</p>
<ul>
  <li>Home Assistant! <ul>
      <li>With preferably <a href="https://www.home-assistant.io/integrations/motioneye/" target="_blank" rel="ugc">MotionEye </a>as a light NVR software for recording </li>
      <li>With <a href="https://esphome.io/guides/getting_started_hassio.html" target="_blank" rel="ugc">ESPHome</a>: </li>
      <li>My YAML configuration of the ESP32 S3 via ESPHOME: <a href="https://github.com/idkjustgoogleit/esp32/blob/main/esp32-s3-doorbell/esp32-s3-doorbell_config" target="_blank" rel="ugc">GitHUB</a>
        <i>( ←this took a lot of time to figure out, enjoy!)</i>
        <br>&nbsp;
      </li>
    </ul>
  </li>
  <li>Soldering iron! (don't use the cheap ones!)</li>
  <li>At least 4 WaGo connectors, or solder cables if you'd prefer</li>
  <li>12v adapter if you want to use night vision, otherwise a good 5v usb chager.</li>
  <li>A few M3 bolts + nuts + screws</li>
  <li>Rubber band (optional)</li>
  <li>16mm metal push button (5v): <a href="https://nl.aliexpress.com/item/4001291695467.html?spm=a2g0o.productlist.main.1.55297f48RBUMdI&amp;algo_pvid=b3fecfd3-cb41-47ac-87cd-85168fa3d798&amp;algo_exp_id=b3fecfd3-cb41-47ac-87cd-85168fa3d798-0&amp;pdp_npi=4%40dis%21EUR%211.14%210.87%21%21%211.21%21%21%40210384b917015207404887289e264c%2110000015640393882%21sea%21NL%21140017539%21&amp;curPageLogUid=kgxzT3EIlgoI" target="_blank" rel="ugc">AliExpress</a>
  </li>
  <li>DuPont cables</li>
  <li>ESP32 S3 Freenove with CAM support: <a href="https://nl.aliexpress.com/item/1005004339923548.html?spm=a2g0o.home.0.0.682e44f506YOyw&amp;mp=1&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
  </li>
  <li>Wide angle camera with long (75mm) cable, like this one:&nbsp; <a href="https://nl.aliexpress.com/item/1005002947160929.html?spm=a2g0o.order_list.order_list_main.30.23b279d22UzMsf&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
    <br>&nbsp;
  </li>
  <li>( <i>This is a tricky one</i>) Transparent flat sheet of plastic; you will need to (eyeball) cut this into a small square with a hole in the middle, which then will serve as protection for the IR LED Ring and ofc the internals of the case. I used a plastic transparent candy box, and re-purposed it accordingly. OR buy this and make your own camera holder: <a href="https://nl.aliexpress.com/item/32815931704.html?spm=a2g0o.order_list.order_list_main.5.662079d25KiHGn&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
    <br>&nbsp;
  </li>
  <li>
    <strong>VERY IMPORTANT:</strong>
    <br>
    <i>You <strong>WILL </strong>NEED a small heatsink </i>to put behind the camera module because they heat up and die. I used an aluminum heatsink which I had laying around for a generic raspberry pi. <br>&nbsp;
  </li>
  <li>
    <strong>IR Night-vision LED Ring:</strong>
    <br>I used this but is not sold anymore: <a href="https://nl.aliexpress.com/item/32861366234.html?spm=a2g0o.order_list.order_list_main.5.118e79d27TB7jQ&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AlieExpress</a>
    <ul>
      <li>
        <strong>Buy this instead</strong> because it has same specs and dimensions: <a href="https://nl.aliexpress.com/item/1005004141393390.html?spm=a2g0o.productlist.main.15.46c0GPOHGPOHHf&amp;algo_pvid=2d91114f-8419-4f2e-b97e-29b3f8778fbd&amp;algo_exp_id=2d91114f-8419-4f2e-b97e-29b3f8778fbd-7&amp;pdp_npi=4%40dis%21EUR%211.05%210.84%21%21%218.06%216.45%21%4021038dfc17105085052202787e75a7%2112000028168061768%21sea%21NL%21140017539%21&amp;curPageLogUid=BpfPQwgfA77H&amp;utparam-url=scene%3Asearch%7Cquery_from%3A" target="_blank" rel="ugc">AliExpress</a>
        <br>&nbsp;
      </li>
      <li>When using these you will need to use a 12v to 5v buck converter to power the 12v IR Led ring AND the ESP32 and etc at 5v at the same time: <a href="https://nl.aliexpress.com/item/32861366234.html?spm=a2g0o.order_list.order_list_main.5.118e79d27TB7jQ&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
      </li>
    </ul>
  </li>
</ul>
<p>
  <strong>Ringer: </strong>The <a href="https://github.com/idkjustgoogleit/esp32/blob/main/esp32-s3-doorbell/esp32-s3-doorbell_config" target="_blank" rel="ugc">YAML Config included</a> relies on a <a href="https://esphome.io/components/dfplayer.html" target="_blank" rel="ugc">DFPlayer module</a> to ring a doorbell chime through a small speaker. Whenever the doorbell button is pressed, the metal push button led light will flash a few times AND will play a mp3 file on the SD-Card of the DFPlayer module:
</p>
<ul>
  <li>DFPlayer module: <a href="https://nl.aliexpress.com/item/1005006027775709.html?spm=a2g0o.order_list.order_list_main.30.662079d25KiHGn&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
  </li>
  <li>Small (intercom) speaker: <a href="https://nl.aliexpress.com/item/1005006056453298.html?spm=a2g0o.order_list.order_list_main.50.662079d25KiHGn&amp;gatewayAdapt=glo2nld" target="_blank" rel="ugc">AliExpress</a>
  </li>
</ul>
<p>&nbsp;</p>
<p>
  <i>
    <strong>Side notes</strong>
  </i>: the IR Night vision LED Ring is too strong :) SO I have solved this by <a href="https://github.com/esphome/esphome/pull/3090" target="_blank" rel="ugc">changing the camera image settings on the fly</a> before and after sunset. This is done via an HomeAssistant automation and 2 scripts:
</p>
<ul>
  <li>After sunrise → trigger automation → set daylight mode using following script: <a href="https://github.com/idkjustgoogleit/esp32/blob/main/esp32-s3-doorbell/HA_Script_doorbell_cam_set_daylight" target="_blank" rel="ugc">HA Script (github)</a>
  </li>
  <li>After sunset → trigger automation → set night mode using following script: <a href="https://github.com/idkjustgoogleit/esp32/blob/main/esp32-s3-doorbell/HA_Script_doorbell_cam_set_night" target="_blank" rel="ugc">HA Script (github)</a>
  </li>
</ul>
<p>As you can see in the images, I have added a preview of the HomeAssistant page which shows the stream and some details. On that page I have added 2 buttons to change the image settings just in case the automation triggers above did not work.</p>
<p>&nbsp;</p>
