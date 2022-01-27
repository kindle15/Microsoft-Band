# Microsoft-Band
Port of the German website and tool for Microsoft Band v1 and v2

https://rabiet.de/bandunlocker/


<!DOCTYPE html>
<html>

  <head>
    <meta charset='utf-8'>
    <meta name="description" content="Band Unlocker">

    <title>Band unlocker</title>

    <style>
      body {
          font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-size: 28px;
          background: #333333;
          color: #fff;
          margin: 0px;
      }

      h1 {
        font-family: Segoe UI,Frutiger,Frutiger Linotype,Dejavu Sans,Helvetica Neue,Arial,sans-serif;
        font-size: 36px;
        font-style: normal;
        font-variant: normal;
        font-weight: 500;
        line-height: 26.4px;
          color:#FFF;
          text-align: center;
      }

      h2 {
          font-size: 32px;
          font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-weight: 500;
          color: #277db6;
          text-align: center;
      }

      h3 {
          font-size: 20px;
          font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
          font-weight: 500;
          color: #36aeff;
      }

      p {
          font-size: 20px;
          font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      }

      td {
          text-align: center;
          border-collapse: collapse;
      }

      #header {
          height: 100px;
          background-color:#222; 
          margin: 0px !important;
          padding: 10px;
          box-sizing:border-box;
          -moz-box-sizing:border-box;
          -webkit-box-sizing:border-box;
      }

      .firstLine td{
          border-bottom: 2px solid white;
      }

      .lastline td{
          border-top: 2px solid white;
      }

      .textbox {
        align-self: center;
        text-align: center;
        border-collapse: collapse;
        margin: 0 auto;
        max-width: 800px;
      }

  </style>

  </head>

  <body>
    <div id="header">
      <h1 id="title">Band unlocker</h1>
      <hr style="border-color:#FFF" />
    </div>

    <!-- MAIN CONTENT -->
    <div style="margin: 8px;" class="outer">
      <section id="main_content" class="inner">
      <div class="textbox">
        <h2>Welcome to the Band Unlocker</h2>

        <p>Band Unlocker is an application that's designed to bypass the OOBE Setup of the Microsoft Band 1 and 2.</p>
        <p>
          Ever since Microsoft shut down the Microsoft Health platform Band owners not only didn't have a proper way to sync their bands, but also had no way of going through the setup when the band was reset.</br>
          This application was made to fix this problem!
        </p>
      </div>
      
      <div class="textbox">
        <h2>Update (31.01.21):</h2>
        <p>The BandUnlocker now also allows loading of the sensor log off the band and exporting the data to .tcx file.</p>
        <p>A big thank you to <a href="https://www.reddit.com/user/OverallLine5/">OverallLine5</a>, who figured out how to interpret the data from the band!</p></br>
        <p>You can download the new version <a href="https://bandunlocker.briosche.de/files/BandUnlocker.exe">here!</a></p>
      </div>

      <div class="textbox">
        <h2>FAQ:</h2>
        <ul>
          <li>
            <h3>Which Microsoft Band version are supported?</h3>
            <p>
              Both versions of the Microsoft Band are supported. The tool has been tested with both in mind.
            </p>
          </li>
          <li>
            <h3>What do I need?</h3>
            <p>
              Here's the list of what you'll need:
              <ul>
                <li><p>A Microsoft Band</p></li>
                <li><p>The standard USB cable</p></li>
                <li><p>A Windows PC (Only tested on Windows 10, older systems might work)</p></li>
                <li><p><a href="https://dotnet.microsoft.com/download/dotnet-framework/net48">.NET Framework 4.8 Runtime</a> (Probably already installed)</p></li>
              </ul>
            </p>
          </li>
          <li>
            <h3>My anti-virus gave a warning! Is this a virus?</h3>
            <p>
              No, this program is only concerned with getting your band to run, nothing else. Anti-Virus software is usually extremely cautious with stuff downloaded from the internet (as it should) but you can ignore it this time. </br>
              Since the source is not (yet!) available, so you'll have to take my word for it if you want to use it.
            </p>
          </li>
          <li>
            <h3>My Band is doing weird things on its own. How do I stop it?</h3>
            <p>
              You device probably is stuck in the retail demo mode. This mode was used in store to show people the device. <br>
              You can hit "Disable retail demo mode" in the lower left corner to try to get it out of that mode.
            </p>
          </li>
          <li>
            <h3>Will this bring back all functionality of the band?</h3>
            <p>
              Not quite. You will be able to use the device like you did back in the days, but there are some restrictions.</br>
              Everything that needs the app on your phone won't work. This includes weather, sync, mail, calendar, notifications ...</br>
              Also, the app usually downloads an ephemeris file from the Microsoft servers to help with GPS acquisition. Since the servers are shut down and I don't have a reference file there is no way I can make this work. GPS WILL work but it WILL take ages (1-5 minutes usually) until you have a lock. 
            </p>
          </li>
        </ul>
      </div>


      <div class="textbox">
        <h2>Tutorial:</h2>
          <p>
            Please read carefully through this tutorial as any slight change might leave you with a permanently bricked band.
            <ol>
              <li>
                <p>
                  Make sure your Band is at least half way charged up and on the setup screen, asking you for either the language or the kind of phone you have. <br>
                  Download the tool from <a href="https://bandunlocker.briosche.de/files/BandUnlocker.exe">here</a> and unpack it. <br>
                  Don't start it yet!
                </p>
              </li>
              <li>
                <p>On your band: Choose the type of phone you have. You need to choose the correct OS, you will not be able to change it later without resetting the band!</p>
              </li>
              <li>
                <p>
                  Go throught the pairing process with your phone. Use the system utility for this (usually the settings app) as the official app won't get you to that point. <br>
                  At the end your band should say something along the lines of "Pairing sucess!"
                </p>
              </li>
              <li>
                <p>
                  Connect your band to your PC with the USB cable and start up the unlocker.<br>
                  On the top left the OOBE Status should read "In Setup" and your device name as well as the serial number should be listed there as shown in the picture.<br>
                  DO NOT CONTINUE IF THE STATUS ISN'T "In Setup"!
                </p>
                <img src="img/first_connected.png" width="100%"/>
              </li>
              <li>
                <p>
                  Click the "Unlock Band" button and read the messages appearing in the middle of the screen while the program is at work.
                  Usually you don't need to do anything but in case of an error you will be notified there.<br>
                  If you have a band version 2 it will restart two times. Windows will play the disconnect sound but don't worry about it.<br>
                  Your band will control itself from here on.</p>
                  <p>Do NOT touch the device until the program tells you to!</p>
                  <p>If everything went right it should look like this:</p>
                </p>
                <img src="img/unlock_completed.png" style="width: 100%;" />
              </li>
              <li>
                <p>
                  Your device is now usable again!
                </p>
                All steps from here on are optional!
              </li>
              <li>
                <p>Should you desire to switch from metric to imperial units you can do so by selecting "Imperial" in the 'Units' box and clicking "Apply settings". If you want you can choose a step goal there, too!</p>
              </li>
              <li>
                <p>You can set the desired step goal by simply putting in the numer in the "Step Goal" box.</p>
              </li>
              <li>
                <p>To get more accurate readings from the band you should set your correct gender, height and your weight.</p>
              </li>
              <li>
                <p>You can switch the themes by selecting one out of the "Theme" combo box. Below the box a few colors will show up that preview the theme.</p>
              </li>
              <li>
                <p>By default only some of the default tiles are enabled on the band, some of which don't make sense without the app.</p>
                <ul>
                  <li>
                    <p>You can remove tiles by selecting on the name of the tile in the list "Installed" and clicking on "Remove"</p>
                  </li>
                  <li>
                    <p>If you want to add some tiles you can select them in the list with the title "Available" and click "Add"</p>
                  </li>
                  <li>
                    <p>Tiles can be reordered by selecting them in the "Installed" list and clicking the up or down arrow</p>
                  </li>
                </ul>
                <p>After making the desired changes you need to click "Apply Settings" for them to take effect.</p>
                
              </li>
            </ol>
          </p>
      </div>

      <div class="textbox">
        <h2>Disclaimer:</h2>
          <p>
            The application was tested on my own MS Bands.</br>
            This doesn't mean it will work without problems for everyone. I do not guarantee that everything will work and usage of the software is at your own risk.</br>
            I am not responsible for any broken devices (not that any device in need of this could be considered usable) and I will not replace your device if it won't turn on.
          </p>
          <p>There are no warranties, I take no responsibility for anything.</br> If you aren't willing to take the risk, please leave now.</p>
          <p>
            I'm also not affiliated with Microsoft in any way, shape or form. I merely wanted to get my own device to work again and thought other people might want that, too.</br>
            If anyone at Microsoft has a problem with me publishing this I will take it down immediately.<sup>1</sup>
          </p>
      </div>

      </section>


      <hr style="border-color:#FFF" />

      <div>
        <p style="font-size: 12px;"><sup>1</sup>Contact: <a href="mailto:band@briosche.de">band@briosche.de</a></p>
        <p style="font-size: 12px;"><a href="https://bandunlocker.briosche.de/files/public_pgp_rabiet.asc">PGP Public Key</a></p> 
      </div>

    </div>

  </body>
</html>
