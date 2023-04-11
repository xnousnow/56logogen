<script lang="ts">
  const blue = [
    '#f0f9ff',
    '#e0f2fe',
    '#bae6fd',
    '#7dd3fc',
    '#38bdf8',
    '#0ea5e9',
    '#0284c7',
    '#0369a1',
    '#075985',
    '#0c4a6e',
    '#082f49',
    '#eff6ff',
    '#dbeafe',
    '#bfdbfe',
    '#93c5fd',
    '#60a5fa',
    '#3b82f6',
    '#2563eb',
    '#1d4ed8',
    '#1e40af',
    '#1e3a8a',
    '#172554',
  ]
  let ytones = [
    '#fffbeb',
    '#fef3c7',
    '#fde68a',
    '#fcd34d',
    '#fbbf24',
    '#f59e0b',
    '#d97706',
    '#b45309',
    '#92400e',
    '#78350f',
    '#451a03',
    '#fefce8',
    '#fef9c3',
    '#fef08a',
    '#fde047',
    '#facc15',
    '#eab308',
    '#ca8a04',
    '#a16207',
    '#854d0e',
    '#713f12',
    '#422006',
  ]
  let gtones = [
    '#f0fdfa',
    '#ccfbf1',
    '#99f6e4',
    '#5eead4',
    '#2dd4bf',
    '#14b8a6',
    '#0d9488',
    '#0f766e',
    '#115e59',
    '#134e4a',
    '#042f2e',
    '#ecfdf5',
    '#d1fae5',
    '#a7f3d0',
    '#6ee7b7',
    '#34d399',
    '#10b981',
    '#059669',
    '#047857',
    '#065f46',
    '#064e3b',
    '#022c22',
    '#f0fdf4',
    '#dcfce7',
    '#bbf7d0',
    '#86efac',
    '#4ade80',
    '#22c55e',
    '#16a34a',
    '#15803d',
    '#166534',
    '#14532d',
    '#052e16',
    '#f7fee7',
    '#ecfccb',
    '#d9f99d',
    '#bef264',
    '#a3e635',
    '#84cc16',
    '#65a30d',
    '#4d7c0f',
    '#3f6212',
    '#365314',
    '#1a2e05',
  ]
  let outlineColor = '#0085FF'
  let Acolor = '#0085FF'
  let yellow = '#FFE600'
  let green = '#69EF00'
  let better6 = false
  let round6 = false
</script>

<h1>다 만들어오기 귀찮아서 만든거</h1>

<main>
  <div id="settings">
    <div class="colors">
      {#each blue as color}
        <input type="radio" name="outlineColor" value={color} id={`${color}out`} bind:group={outlineColor} />
        <label for={`${color}out`} style="background-color: {color}"></label>
      {/each}
    </div>
    <div class="colors">
      {#each blue as color}
        <input type="radio" name="Acolor" value={color} id={`${color}A`} bind:group={Acolor} />
        <label for={`${color}A`} style="background-color: {color}"></label>
      {/each}
    </div>
    <div class="colors">
      {#each ytones as color}
        <input type="radio" name="yellow" value={color} id={`${color}y`} bind:group={yellow} />
        <label for={`${color}y`} style="background-color: {color}"></label>
      {/each}
    </div>
    <div class="colors">
      {#each gtones as color}
        <input type="radio" name="green" value={color} id={`${color}g`} bind:group={green} />
        <label for={`${color}g`} style="background-color: {color}"></label>
      {/each}
    </div>
    <label class="checkbox" for="better6">
      <input type="checkbox" id="better6" bind:checked={better6} />
      <div class="fakecheckbox"></div>
      <span>6 손잡이 모양 줄이기</span>
    </label>
    <label class="checkbox" for="round6">
      <input type="checkbox" id="round6" bind:checked={round6} />
      <div class="fakecheckbox"></div>
      <span>저건 진짜 6이 아니야!</span>
  </div>
  <div id="result">
    <svg width="500" height="500" viewBox="0 0 500 500" fill="none" xmlns="http://www.w3.org/2000/svg">
      <rect width="500" height="500" fill="white"/>
      <path fill-rule="evenodd" clip-rule="evenodd" d="M249.5 451.011C360.239 451.011 450.011 361.239 450.011 250.5C450.011 139.761 360.239 49.9891 249.5 49.9891C138.761 49.9891 48.9891 139.761 48.9891 250.5C48.9891 361.239 138.761 451.011 249.5 451.011ZM249.5 487C380.115 487 486 381.115 486 250.5C486 119.885 380.115 14 249.5 14C118.885 14 13 119.885 13 250.5C13 381.115 118.885 487 249.5 487Z" fill={outlineColor}/>
      <path fill-rule="evenodd" clip-rule="evenodd" d="M246.5 102C255.033 102 262.679 107.262 265.714 115.222L355.651 351.181C359.688 361.772 354.358 373.624 343.747 377.654C333.135 381.683 321.261 376.363 317.224 365.772L246.5 180.222L175.776 365.772C171.739 376.363 159.865 381.683 149.253 377.654C138.642 373.624 133.312 361.772 137.349 351.181L227.286 115.222C230.321 107.262 237.967 102 246.5 102Z" fill={Acolor}/>
      <path fill-rule="evenodd" clip-rule="evenodd" d="M105.543 168.239C105.543 159.721 112.449 152.815 120.967 152.815H218.652C227.171 152.815 234.076 159.721 234.076 168.239C234.076 176.758 227.171 183.663 218.652 183.663H136.391V224.003H177.126C208.579 224.003 234.076 249.5 234.076 280.952C234.076 312.405 208.579 337.902 177.126 337.902H120.967C112.449 337.902 105.543 330.997 105.543 322.478C105.543 313.96 112.449 307.054 120.967 307.054H177.126C191.542 307.054 203.228 295.368 203.228 280.952C203.228 266.537 191.542 254.85 177.126 254.85H120.967C112.449 254.85 105.543 247.945 105.543 239.426V168.239Z" fill={yellow}/>
      {#if !better6 && !round6}
        <path fill-rule="evenodd" clip-rule="evenodd" d="M259.783 239.426C259.783 191.592 298.56 152.815 346.394 152.815H372.891C381.41 152.815 388.315 159.721 388.315 168.239C388.315 176.758 381.41 183.663 372.891 183.663H346.394C320.947 183.663 299.482 200.707 292.791 224.003H331.365C362.818 224.003 388.315 249.5 388.315 280.952C388.315 312.405 362.818 337.902 331.365 337.902H324.049C288.556 337.902 259.783 309.129 259.783 273.636V239.426ZM290.63 254.85V273.636C290.63 292.092 305.592 307.054 324.049 307.054H331.365C345.781 307.054 357.467 295.368 357.467 280.952C357.467 266.537 345.781 254.85 331.365 254.85H290.63Z" fill={green} />
      {:else if round6}
        <path fill-rule="evenodd" clip-rule="evenodd" d="M293.848 223.838C293.848 203.961 309.961 187.848 329.838 187.848H365.828C374.346 187.848 381.252 180.943 381.252 172.424C381.252 163.906 374.346 157 365.828 157H329.838C292.924 157 263 186.924 263 223.838V285.535C263 316.769 288.321 342.09 319.555 342.09H334.979C366.214 342.09 391.535 316.769 391.535 285.535C391.535 254.3 366.214 228.979 334.979 228.979H319.555C310.298 228.979 301.561 231.203 293.848 235.146V223.838ZM293.848 285.535C293.848 299.732 305.358 311.242 319.555 311.242H334.979C349.177 311.242 360.686 299.732 360.686 285.535C360.686 271.337 349.177 259.828 334.979 259.828H319.555C305.358 259.828 293.848 271.337 293.848 285.535Z" fill={green} />
      {:else}
        <path fill-rule="evenodd" clip-rule="evenodd" d="M259.783 239.426C259.783 191.592 298.56 152.815 346.394 152.815H365.891C374.41 152.815 381.315 159.721 381.315 168.239C381.315 176.758 374.41 183.663 365.891 183.663H346.394C320.947 183.663 299.482 200.707 292.791 224.003H331.365C362.818 224.003 388.315 249.5 388.315 280.952C388.315 312.405 362.818 337.902 331.365 337.902H324.049C288.556 337.902 259.783 309.129 259.783 273.636V239.426ZM290.63 254.85V273.636C290.63 292.092 305.592 307.054 324.049 307.054H331.365C345.781 307.054 357.467 295.368 357.467 280.952C357.467 266.537 345.781 254.85 331.365 254.85H290.63Z" fill={green} />
      {/if}
    </svg>
  </div>
</main>

<style>
  h1 {
    text-align: center;
    margin-top: 30px;
  }
  main {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    height: 80vh;
  }
  #settings {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
  }
  .colors {
    display: grid;
    grid-template-columns: repeat(11, 1fr);
    border-radius: 10px;
    overflow: hidden;
    grid-gap: 0;
  }
  input[type="radio"] {
    display: none;
  }
  label {
    display: inline-block;
    width: 50px;
    height: 50px;
    box-sizing: border-box;
    cursor: pointer;
  }
  input[type="radio"]:checked + label {
    border: 4px solid black;
  }
  input[type="checkbox"] {
    display: none;
  }
  .checkbox {
    display: flex;
    align-items: center;
    gap: 8px;
    margin: 0 auto;
    width: auto;
    cursor: pointer;
  }
  .fakecheckbox {
    display: inline-block;
    width: 2rem;
    height: 2rem;
    border: 1px solid rgba(0, 0, 0, 0.2);
    border-radius: 5px;
    box-sizing: border-box;
  }
  input[type="checkbox"]:checked + .fakecheckbox {
    background-color: #0085FF;
    border: 2px solid #0076e4;
  }
  span {
    width: auto;
    height: auto;
    font-size: 1.5rem;
  }
</style>
