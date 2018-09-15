# ProTally
On-screen tally software for use with products like ProPresenter or ProVideoServer, enabling the operator to know when their source is visible on-air in a TSL 3.1 protocol environment, like a Ross Carbonite switcher.
<div>
<div id="divLicense">
                Copyright 2018 Joseph Adams.<br /><br />
                Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
<br /><br />
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
<br /><br />
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
                </div><br /><br />
            It is not sold, authorized, or associated in any way with any other company or product.<br /><br />
            To contact the author or for more information, please visit <a id="bloglink" href="#">www.techministry.blog</a>.
            <br /><br />
            <b>HOW TO USE THIS PROGRAM:</b><br /><br />
            Open the ProTally <a id="settingslink" href="#">Settings</a> menu.<br /><br />
            <i>You can choose one of the following supported devices:</i><br />
                <ul>
                    <li>Ross Carbonite</li>
                    <li>Ross Carbonite Black</li>
                    <li>Ross Carbonite Black Solo</li>
                    <li>Ross Graphite</li>
                    <li>Generic TSL 3.1 Device<br />
                    Your TSL device should send data in this format:<br />
                    <pre>
{
    address: 90,
    brightness: 3,
    tally4: 0,
    tally3: 0,
    tally2: 0,
    tally1: 0,
    label: '      LABEL     '
}
                    </pre>
                    Tally1 typically represents the <i>Preview</i> state and Tally2 typically represents the <i>Program</i> state. Tally3 and Tally 4 are not implemented in ProTally.
                    </li>
                  <li>Blackmagic ATEM</li>
                </ul>
            <i>Using a Ross Carbonite, Carbonite Black, Carbonite Black Solo, or Graphite Switcher:</i><br />
            <ul>
                <li>On your Ross switcher, configure a new device with these settings:
                    <ul>
                        <li>IP Address: <span id="spanRossIPAddresses"></span></li>
                        <li>Port: <span id="spanRossPort"></span></li>
                        <li>Transport Type: UDP</li>
                    </ul>   
                </li>
                <li>Select the Ross device type you are using in the device list at the top of the Settings menu.</li>
                <li>Make sure the Port number matches what you specified on your Ross device.</li>
                <li>Select "UDP" as the protocol type.</li>
                <li>Click "Connect".</li>
            </ul>
            <i>Using the TSL UMD 3.1 Protocol:</i><br />
            <ul>
                <li>On your Tally server (ImageVideo TSI 4000, etc.), configure a client with these settings:
                    <ul>
                        <li>IP Address: <span id="spanTSLIPAddresses"></span></li>
                        <li>Port: <span id="spanTSLPort"></span></li>
                        <li>Transport Type: TCP or UDP</li>
                    </ul>
                </li>
                <li>In ProTally, select "Generic TSL 3.1 Device" in the device list at the top of the Settings menu.</li>
                <li>Make sure the Port number matches what you specified on your Tally server.</li>
                <li>Click "Connect".</li>
            </ul>
            <br />
          <i>Using a Blackmagic ATEM:</i><br />
            <ul>
                <li>Select "Blackmagic ATEM" in the device list at the top of the settings menu.</li>
                <li>If your Blackmagic ATEM Switcher is not in the drop down list, it was not detected automatically on the network. Choose "manual entry" from the list and type in the IP address of your switcher.</li>
                <li>Click "Connect".</li>
            </ul>
            <b><i>Click "Disconnect" to stop listening for device tally data at any time.</i></b>
            <br />
            <b>Specifying Tally Addresses:</b><br />
            <ul>
                <li>ProTally supports up to 4 Tally Windows.</li>
                <li>Enter an address (input number) into a Tally Address field.</li>
                <li>To disable a particular Tally Box, enter "0" into the Tally Address field.</li>
                <li>If you are not using a generic TSL 3.1 device, ProTally supports using the default addresses. The labels will update as the tally data is received. Click "Use Device-Specific Tally Addresses" to take advantage of this feature rather than typing in the address numbers manually.</li>
                <li>Tally Boxes can either be displayed as transparent boxes with a color border, or as a filled-in box. The transparent box is turned on by default.</li>
                <li>Tally Boxes can display the label, if the name is known and transmitted with the tally data.</li>
                <li>To resize/position a tally box, click "Resize/Move" for that box. The Tally Box will appear on the screen. When you are finished, click "Save Window Position".</li>
                <li>Update all desired Tally Address fields and choose "Update Tally Settings" at the bottom of the menu to save the settings.</li>
            </ul>
            <b><i>Special Notes:</i></b><br />
            <ul>
                <li>Tally Windows will display on top of all other windows. To temporarily hide them, choose "Hide All Boxes" from the tray menu.</li>
                <li>Preview, Program, and Preview+Program (when an input is set to both) colors can be customized. Some TSL devices will send Preview data in Tally 2 with Program in Tally 1, whereas ProTally expects the opposite. If this is the case, simply change the colors to match the state desired. Click "Update Tally Settings" to save color changes.</li>
            </ul>
            </div>
