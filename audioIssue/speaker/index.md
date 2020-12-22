<style>
.accordion {
  background-color: #eee;
  color: #444;
  cursor: pointer;
  padding: 18px;
  width: 100%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
  transition: 0.4s;
}

.active, .accordion:hover {
  background-color: #ccc;
}

.accordion:after {
  content: '\002B';
  color: #777;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.active:after {
  content: "\2212";
}

.panel {
  padding: 0 18px;
  background-color: white;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.2s ease-out;
}
</style>

<button id="unable_hear_claimant" class="accordion">I am unable to hear the claimant</button>
<div class="panel">
<h2 id="exclusive_control">Make sure Teams can’t take exclusive control of the speaker.</h2>
<br />
1. Search for Control Panel in the Windows search bar and open it up

![Control Panel](./control_panel.jpg)

2. In the top right, switch to View by: Large icons

![Control Panel Large Icons](./control_panel_switch_to_large_icons.jpg)

3. Click on Sound

![Control Panel Sound](./control_panel_sound.jpg)

4. On Playback tab, right click the active output device (for example, Jabra headset or AirPods)

5. Go to Properties

6. Go to Advanced tab and Uncheck "Allow applications to take exclusive control of this device".

7. Click OK
</div>
<button id="browser_permission_sound" class="panel">Check if your browser has permission to play sounds</button>
<div class="panel">
1. In the Cortana search bar, search for “Sound mixer options”

2. Ensure that Chrome and/or Firefox is unmuted.

3. Change the input of the browser to your microphone.

4. Change the output of the browser to your headset.
</div>

<script>
var acc = document.getElementsByClassName("accordion");
var i;

for (i = 0; i < acc.length; i++) {
  acc[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var panel = this.nextElementSibling;
    if (panel.style.maxHeight) {
      panel.style.maxHeight = null;
    } else {
      panel.style.maxHeight = panel.scrollHeight + "px";
    } 
  });
}
</script>