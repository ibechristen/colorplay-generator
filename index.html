<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ColorPlay Generator</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: #f5f5f5;
      color: #222;
    }
    .wrap {
      max-width: 1100px;
      margin: 0 auto;
      padding: 24px;
    }
    h1 {
      margin: 0 0 8px;
      font-size: 32px;
    }
    .sub {
      margin: 0 0 24px;
      color: #555;
      line-height: 1.5;
    }
    .grid {
      display: grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap: 24px;
    }
    .card {
      background: white;
      border-radius: 18px;
      padding: 20px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.06);
      margin-bottom: 24px;
    }
    .card h2 {
      margin-top: 0;
      font-size: 22px;
    }
    .field {
      margin-bottom: 18px;
    }
    label {
      display: block;
      font-weight: 700;
      margin-bottom: 8px;
    }
    input[type="range"] {
      width: 100%;
    }
    select, input[type="number"], input[type="text"] {
      width: 100%;
      padding: 10px 12px;
      border: 1px solid #ccc;
      border-radius: 10px;
      font-size: 16px;
    }
    .value {
      font-size: 14px;
      color: #666;
      margin-top: 6px;
    }
    .preview {
      height: 290px;
      border-radius: 16px;
      border: 1px solid #ddd;
      margin-bottom: 18px;
    }
    .info-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
      margin-top: 14px;
    }
    .mini {
      border: 1px solid #e1e1e1;
      border-radius: 14px;
      padding: 14px;
      background: #fff;
    }
    .recipe {
      margin-top: 14px;
      background: #f2f2f2;
      border-radius: 12px;
      padding: 14px;
      font-weight: 700;
      line-height: 1.5;
    }
    .btn-row {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-top: 16px;
    }
    button {
      border: none;
      background: #111;
      color: white;
      padding: 11px 15px;
      border-radius: 10px;
      cursor: pointer;
      font-size: 15px;
    }
    button.alt {
      background: #eaeaea;
      color: #222;
    }
    .anchor-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }
    .anchor {
      border: 1px solid #e2e2e2;
      border-radius: 12px;
      padding: 12px;
      background: #fff;
    }
    .hint {
      color: #666;
      font-size: 14px;
      line-height: 1.5;
      margin-top: 8px;
    }
    @media (max-width: 900px) {
      .grid { grid-template-columns: 1fr; }
      .info-grid, .anchor-grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <div class="wrap">
    <h1>ColorPlay Generator</h1>
    <p class="sub">
      Standalone version. Pick a Base Color, adjust Hue, Saturation, and Brightness, and use the live preview.
      This uses standard anchor degrees under the hood so you can compare ColorPlay values to HSV-style hue.
    </p>

    <div class="grid">
      <div>
        <div class="card">
          <h2>ColorPlay Controls</h2>

          <div class="field">
            <label for="base">Base Color</label>
            <select id="base">
              <option value="Red">Red (0°)</option>
              <option value="Yellow" selected>Yellow (60°)</option>
              <option value="Green">Green (120°)</option>
              <option value="Cyan">Cyan (180°)</option>
              <option value="Blue">Blue (240°)</option>
              <option value="Magenta">Magenta (300°)</option>
            </select>
          </div>

          <div class="field">
            <label for="adjust">Hue Adjust</label>
            <input id="adjust" type="range" min="-255" max="255" value="27" step="1" />
            <div class="value">Current: <span id="adjustValue">27</span></div>
            <div class="hint">Negative usually shifts warmer. Positive usually shifts cooler.</div>
          </div>

          <div class="field">
            <label for="saturation">Saturation</label>
            <input id="saturation" type="range" min="0" max="100" value="67" step="1" />
            <div class="value">Current: <span id="saturationValue">67</span></div>
          </div>

          <div class="field">
            <label for="brightness">Brightness</label>
            <input id="brightness" type="range" min="0" max="100" value="100" step="1" />
            <div class="value">Current: <span id="brightnessValue">100</span></div>
          </div>

          <div class="btn-row">
            <button class="alt" id="resetBtn">Reset Example</button>
            <button id="copyBtn">Copy Recipe</button>
          </div>
        </div>

        <div class="card">
          <h2>Convert from Standard HSV Hue</h2>
          <div class="field">
            <label for="manualHue">Hue (0–360)</label>
            <input id="manualHue" type="number" min="0" max="360" value="87" />
          </div>
          <div class="btn-row">
            <button id="convertBtn">Convert</button>
          </div>
          <div class="hint" id="convertResult">Suggested mapping will appear here.</div>
        </div>
      </div>

      <div>
        <div class="card">
          <div id="preview" class="preview"></div>

          <div class="info-grid">
            <div class="mini">
              <strong>ColorPlay</strong>
              <div>Base: <span id="infoBase"></span></div>
              <div>Hue Adjust: <span id="infoAdjust"></span></div>
              <div>Saturation: <span id="infoSat"></span></div>
              <div>Brightness: <span id="infoBright"></span></div>
            </div>
            <div class="mini">
              <strong>Standard HSV / RGB</strong>
              <div>Hue: <span id="infoHue"></span>°</div>
              <div>Saturation: <span id="infoSat2"></span>%</div>
              <div>Brightness: <span id="infoBright2"></span>%</div>
              <div>RGB: <span id="infoRgb"></span></div>
              <div>HEX: <span id="infoHex"></span></div>
            </div>
          </div>

          <div class="recipe" id="recipe"></div>
        </div>

        <div class="card">
          <h2>Base Anchor Degrees</h2>
          <div class="anchor-grid">
            <div class="anchor"><strong>Red</strong><br>0°</div>
            <div class="anchor"><strong>Yellow</strong><br>60°</div>
            <div class="anchor"><strong>Green</strong><br>120°</div>
            <div class="anchor"><strong>Cyan</strong><br>180°</div>
            <div class="anchor"><strong>Blue</strong><br>240°</div>
            <div class="anchor"><strong>Magenta</strong><br>300°</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <script>
    const BASES = {
      Red: 0,
      Yellow: 60,
      Green: 120,
      Cyan: 180,
      Blue: 240,
      Magenta: 300
    };

    const baseEl = document.getElementById('base');
    const adjustEl = document.getElementById('adjust');
    const saturationEl = document.getElementById('saturation');
    const brightnessEl = document.getElementById('brightness');
    const manualHueEl = document.getElementById('manualHue');

    const adjustValueEl = document.getElementById('adjustValue');
    const saturationValueEl = document.getElementById('saturationValue');
    const brightnessValueEl = document.getElementById('brightnessValue');

    const previewEl = document.getElementById('preview');
    const infoBaseEl = document.getElementById('infoBase');
    const infoAdjustEl = document.getElementById('infoAdjust');
    const infoSatEl = document.getElementById('infoSat');
    const infoBrightEl = document.getElementById('infoBright');
    const infoHueEl = document.getElementById('infoHue');
    const infoSat2El = document.getElementById('infoSat2');
    const infoBright2El = document.getElementById('infoBright2');
    const infoRgbEl = document.getElementById('infoRgb');
    const infoHexEl = document.getElementById('infoHex');
    const recipeEl = document.getElementById('recipe');
    const convertResultEl = document.getElementById('convertResult');

    function wrapHue(deg) {
      let out = deg % 360;
      if (out < 0) out += 360;
      return out;
    }

    function hsvToRgb(h, s, v) {
      s = s / 100;
      v = v / 100;
      const c = v * s;
      const x = c * (1 - Math.abs((h / 60) % 2 - 1));
      const m = v - c;
      let r = 0, g = 0, b = 0;

      if (h >= 0 && h < 60) { r = c; g = x; b = 0; }
      else if (h < 120) { r = x; g = c; b = 0; }
      else if (h < 180) { r = 0; g = c; b = x; }
      else if (h < 240) { r = 0; g = x; b = c; }
      else if (h < 300) { r = x; g = 0; b = c; }
      else { r = c; g = 0; b = x; }

      return {
        r: Math.round((r + m) * 255),
        g: Math.round((g + m) * 255),
        b: Math.round((b + m) * 255)
      };
    }

    function rgbToHex(r, g, b) {
      return '#' + [r, g, b].map(v => v.toString(16).padStart(2, '0')).join('').toUpperCase();
    }

    function nearestBase(hue) {
      let best = null;
      for (const [name, deg] of Object.entries(BASES)) {
        const forward = wrapHue(hue - deg);
        const signed = forward > 180 ? forward - 360 : forward;
        const distance = Math.abs(signed);
        if (!best || distance < best.distance) {
          best = { name, deg, adjust: Math.round(signed), distance };
        }
      }
      return best;
    }

    function render() {
      const base = baseEl.value;
      const adjust = Number(adjustEl.value);
      const saturation = Number(saturationEl.value);
      const brightness = Number(brightnessEl.value);
      const baseDeg = BASES[base];
      const hue = wrapHue(baseDeg + adjust);
      const rgb = hsvToRgb(hue, saturation, brightness);
      const hex = rgbToHex(rgb.r, rgb.g, rgb.b);
      const recipe = `Base: ${base} | Hue Adjust: ${adjust} | Saturation: ${saturation} | Brightness: ${brightness}`;

      adjustValueEl.textContent = adjust;
      saturationValueEl.textContent = saturation;
      brightnessValueEl.textContent = brightness;

      previewEl.style.background = hex;
      infoBaseEl.textContent = base;
      infoAdjustEl.textContent = adjust;
      infoSatEl.textContent = saturation;
      infoBrightEl.textContent = brightness;
      infoHueEl.textContent = hue;
      infoSat2El.textContent = saturation;
      infoBright2El.textContent = brightness;
      infoRgbEl.textContent = `${rgb.r}, ${rgb.g}, ${rgb.b}`;
      infoHexEl.textContent = hex;
      recipeEl.textContent = recipe;

      const suggestion = nearestBase(hue);
      convertResultEl.textContent = `Suggested mapping for current preview: ${suggestion.name} with Hue Adjust ${suggestion.adjust}`;
    }

    document.getElementById('resetBtn').addEventListener('click', () => {
      baseEl.value = 'Yellow';
      adjustEl.value = 27;
      saturationEl.value = 67;
      brightnessEl.value = 100;
      manualHueEl.value = 87;
      render();
    });

    document.getElementById('copyBtn').addEventListener('click', async () => {
      try {
        await navigator.clipboard.writeText(recipeEl.textContent);
        alert('Recipe copied.');
      } catch (e) {
        alert('Clipboard copy was blocked in this browser.');
      }
    });

    document.getElementById('convertBtn').addEventListener('click', () => {
      const hue = wrapHue(Number(manualHueEl.value || 0));
      const match = nearestBase(hue);
      baseEl.value = match.name;
      adjustEl.value = Math.max(-255, Math.min(255, match.adjust));
      render();
      convertResultEl.textContent = `Input hue ${hue}° → Base ${match.name}, Hue Adjust ${match.adjust}`;
    });

    [baseEl, adjustEl, saturationEl, brightnessEl].forEach(el => {
      el.addEventListener('input', render);
      el.addEventListener('change', render);
    });

    render();
  </script>
</body>
</html>
