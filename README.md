<!DOCTYPE html>
<html class="no-js" lang="en">
  <head>
  </head>
  <body>
    <div class="wrapAll clearfix">
      <div class="mainsection"><br>
        <div class="article">
          <h1><span style="color: rgb(0, 0, 0); font-family: &quot;Times
              New Roman&quot;; font-size: 26.6667px; font-style: normal;
              font-variant-ligatures: normal; font-variant-caps: normal;
              font-weight: 400; letter-spacing: normal; orphans: 2;
              text-align: start; text-indent: 0px; text-transform: none;
              white-space: normal; widows: 2; word-spacing: 0px;
              -webkit-text-stroke-width: 0px; text-decoration-style:
              initial; text-decoration-color: initial; display: inline
              !important; float: none;">DFM-06 Modification to GPS-Mouse</span>
          </h1>
          <p class="siteSub">
          </p>
          <div class="articleRight"> <img src="img/dfm06.png"
              alt="dfm06" width="53" height="65"><br>
          </div>
          <br>
          The DFM-06 is a series of small single-board Radiosonde's
          developed by Graw to carry out meteo soundings.<br>
          Inside houses a GPS Jupiter Telit JN3.<br>
          If the job is done, they are useless..<span style="color:
            rgb(0, 0, 0); font-family: Verdana, Arial, Helvetica,
            sans-serif; font-size: 13.3333px; font-style: normal;
            font-variant-ligatures: normal; font-variant-caps: normal;
            font-weight: 400; letter-spacing: normal; orphans: 2;
            text-align: left; text-indent: 0px; text-transform: none;
            white-space: normal; widows: 2; word-spacing: 0px;
            -webkit-text-stroke-width: 0px; background-color: rgb(239,
            239, 239); text-decoration-style: initial;
            text-decoration-color: initial; display: inline !important;
            float: none;"></span><br>
          But they can be recycled to GPS Mouse.<br>
          <br>
          <div class="contentsPanel">
            <div class="contentsHeader">Contents:</div>
            <ul>
              <li> <span></span>Overview
                <ul>
                  <li><span>1.1&nbsp; <a href="#Hardware_Details">Hardware
                        Details</a></span> </li>
                  <li><span>1.2&nbsp; <a href="#Needed_stuff_">Needed
                        stuff&nbsp;</a></span> </li>
                  <li><span>1.3&nbsp;<a href="#DFM-06_JN3_Modification_">
                        DFM-06 JN3 Mod.</a><br>
                    </span></li>
                  <li><span>1.4&nbsp; <a
                        href="#Windows_SirfNMEA_Mode_JN3">Windows
                        Sirf/NMEA</a></span><br>
                  </li>
                  <li><span>1.5</span><a href="#Linux_NMEASirf_">Linux
                      NMEA/Sirf mode</a><a
                      href="#Zilog_i-Met4_Decoder_Scripts"><br>
                    </a></li>
                </ul>
              </li>
            </ul>
          </div>
          <h2><a name="Hardware_Details"></a>Hardware Details<br>
          </h2>
          <br>
          DFM-06 Details: <a href="https://www.gruan.org/instruments/radiosondes/sonde-models/graw-dfm-06/"
            target="_blank">https://www.gruan.org/instruments/radiosondes/sonde-models/graw-dfm-06/</a>
          <div class="articleRight"><br><img src="img/JN3.jpg?raw=true" alt="ref"
              width="305" height="190">&nbsp; <br>
            Telit JN3 Reference Design
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <br>
          </div>
          <br>
          Telit Jupiter JN3 Details: <a
href="https://www.telit.com/m2m-iot-products/positioning-timing-modules/positioning-gps-jupiter-n3/"
            target="_blank">https://www.telit.com/m2m-iot-products/positioning-timing-modules/positioning-gps-jupiter-n</a><br>
          <br>
          GPS chips are often used on Radiosonde's to get a accurate
          position. <br>
          The JN3 uses SIRF at 9600Baud.<br>
          <br>
          <h2><a name="Needed_stuff_"></a>Needed stuff<br>
          </h2>
          <img src="img/sku_224704_1_small.jpg" alt="ttl" width="140"
            height="140"><br>
          DFM-06.<br>
          USB-TTL converter.<br>
          Some wires.<br>
          Soldering tools.<br>
          <br>
          <h2><a name="DFM-06_JN3_Modification_"></a>DFM-06 JN3
            Modification<br>
          </h2>
          <br>
          Remove the Batteries.<br>
          Desolder 4 legs and remove tuner print and
          Sensor arm.
          <p>Wire pin 20 TX and pin 21 RX on JN3 GPS Module.</p>
          <p>Wire on brown condesator above, left +3.3V and right -GND.
          </p>
          <p>And solder TTL-USB converter on 4 tiny pins bottom right
            from JN3 GPS module:</p>
          <p>Build together -&gt;</p>
          <img src="img/DFM_GPS.jpg" alt="build" width="379"
            height="382"> <br>
          <h2><a name="Windows_SirfNMEA_Mode_JN3"></a>Windows Sirf/NMEA
            Mode JN3</h2>
          <p>Connect with USB cable to computer.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          </p>
          <p>Download and start <a
              href="https://www.falcom.de/support/software-tools/sirf/"
              target="_blank">SirfDemo </a>select COM Port (most
            probaly <a
href="http://www.prolific.com.tw/US/ShowProduct.aspx?p_id=225&amp;pcid=41"
              target="_blank">Prolific driver</a> is needed on Windows)
            and use 9600 Baud to connect.<br>
            <br>
          </p>
          <img src="img/Sirf_demo-1.jpg" alt="sirf" width="421"
            height="311">
          <p>JN3 starts itself in Binary Sirf mode.</p>
          <img src="img/Output.JPG" alt="bin" width="288" height="243">
          <p>From action menu choose Switch to NMEA Protocol.</p>
          <p>Choose a desired Baudrate.</p>
          <img src="img/Sirf_demo-2.jpg" alt="buadrate" width="418"
            height="299">
          <p>DFM-06 works in NMEA 4800 Baud mode.</p>
          <img src="img/SirfDemo-3.jpg" alt="gps2" width="416"
            height="298">
          <p>Can use any GPS Application know.</p>
          <img src="img/Visual_GPS.jpg" alt="vis gps" width="420"
            height="286"><br>
          <p>But remember to follow whole procedure again when
            disconnecting the GPS Mouse, it will start again in Binairy
            Sirf Mode..</p>
          <p>A <a href="/GPS_Com1.bat?raw=true">batch file</a> can be made
            for auto startup GPS mouse in NMEA Mode .</p>
          <p>Example Com:1 4800 Baud:</p>
          <p>@echo off</p>
          <p>echo Switching DFM to GPS mouse.</p>
          <p>mode com1 baud=9600 parity=n data=8 stop=1</p>
          <p>copy sirfbinary2nmea.txt com1:</p>
          <p>echo&nbsp; 4800 baud.</p>
          <p> </p>
          <h2><a name="Linux_NMEASirf_"></a>Linux NMEA/Sirf<br>
          </h2>
          <p>In Linux no drivers are needed to install.<br>
          </p>
          <p>For Sifrmode on the 9600 JN3 Short Version a script can be
            made:<br>
          </p>
          <p><a href="/sirfbinary2nmea.txt?raw=true">sirfbinary2nmea.txt</a></p>
          <p>Make dfm.sh</p>
          <p>#!/bin/sh</p>
          <p>dmesg | grep ttyUSB0</p>
          <p>echo "Switch DFM06 from binary 2 NMEA mode..."</p>
          <p>cd /home/gps</p>
          <p>sudo stty -F /dev/ttyUSB0 speed 9600</p>
          <p>echo "Insert sirfbinary2nmea..."</p>
          <p>cat sirfbinary2nmea.txt &gt; /dev/ttyUSB0</p>
          <p>echo "Switch to 4800 Baud..."</p>
          <p>sudo stty -F /dev/ttyUSB0 speed 4800</p>
          <p>echo "Done DFM on 4800 Baud"<br>
            <br>
          </p>
          <p> </p>
          <p>Before make some sudo chown -R &lt;username:username&gt;
            /dev/ttyUSB0</p>
          <p>You can use GPSD with some build in apps or use
            FoxtrotGPS/Viking.<br>
            <br>
          </p>
          <img src="img/GPSMon.jpg" alt="gpsmon" width="577"
            height="397"><br>
          <p>gpsd /dev/ttyUSB0</p>
          <p> </p>
          <p><br>
            NMEA Mode:<br>
            dmesg | grep ttyUSB</p>
          <p>xgps /dev/ttyUSB0</p>
          <p>cgps -s</p>
          <p>gpsmon /dev/ttyUSB0</p>
          <p><a
href="https://wiki.winehq.org/index.php?title=Wine_User%27s_Guide&amp;oldid=2519#Serial_and_Parallel_Ports"
              target="_blank">Make it work in Wine</a><br>
            <br>
          </p>
          <p> </p>
          Note: <br>
          <p>Some tutorials floating arround the net show a DFM with
            batteries connected,</p>
          <p>So it can store NMEA mode in memory, for continous usage
            its not safe due the +3.3V, they can explode...</p>
          <br>
          <img src="img/burn.jpg" alt="ai" width="350" height="467"><br>
          <br>
        </div>
        <div class="pagefooter">
          <p>Thanks fly out to Zauberkopf.</p>
  </body>
</html>
