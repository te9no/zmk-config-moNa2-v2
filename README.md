![mona2 Keymap](keymap-drawer/moNa2.svg)




<!-- ====== Dynamic Layer Switcher (Solstice/Nihei Style) ====== -->
<style>
/* Container */
.layer-switcher {
  background: #0d1829;
  border: 1px solid #1a2b49;
  padding: 14px;
  border-radius: 12px;
  margin: 16px 0;
  box-shadow: 0 0 12px rgba(20,40,80,0.4);
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}

/* Hide radios */
.layer-switcher input[type="radio"] {
  display: none;
}

/* Buttons */
.layer-button {
  display: inline-block;
  background: rgba(22,35,65,0.85);
  padding: 6px 12px;
  margin: 0 6px 10px 0;
  border: 1px solid #2f4c7d;
  color: #c9d8ef;
  border-radius: 6px;
  cursor: pointer;
  font-size: 14px;
  transition: 0.15s ease;
}

.layer-button:hover {
  background: #1c2f50;
  transform: translateY(-1px);
  box-shadow: 0 0 6px rgba(80,120,255,0.3);
}

/* Active button highlight */
#layer0:checked ~ .buttons label[for="layer0"],
#layer1:checked ~ .buttons label[for="layer1"],
#layer2:checked ~ .buttons label[for="layer2"],
#layer3:checked ~ .buttons label[for="layer3"] {
  background: #2a4a7c;
  border-color: #6fa8ff;
  box-shadow: 0 0 6px rgba(120,160,255,0.4);
}

/* Content Area */
.layer-content { display: none; margin-top: 10px; }
.layer-content img { max-width: 100%; border-radius: 8px; }

#layer0:checked ~ #content0,
#layer1:checked ~ #content1,
#layer2:checked ~ #content2,
#layer3:checked ~ #content3 {
  display: block;
}
</style>


<div class="layer-switcher">

  <!-- Radios -->
  <input type="radio" id="layer0" name="layer" checked>
  <input type="radio" id="layer1" name="layer">
  <input type="radio" id="layer2" name="layer">
  <input type="radio" id="layer3" name="layer">

  <!-- Buttons -->
  <div class="buttons">
    <label for="layer0" class="layer-button">Base</label>
    <label for="layer1" class="layer-button">Raise</label>
    <label for="layer2" class="layer-button">Lower</label>
    <label for="layer3" class="layer-button">Adjust</label>
  </div>

  <!-- Contents -->
  <div id="content0" class="layer-content">
    <img src="img/layer_base.svg">
  </div>

  <div id="content1" class="layer-content">
    <img src="img/layer_raise.svg">
  </div>

  <div id="content2" class="layer-content">
    <img src="img/layer_lower.svg">
  </div>

  <div id="content3" class="layer-content">
    <img src="img/layer_adjust.svg">
  </div>

</div>
<!-- ====== End Layer Switcher ====== -->
