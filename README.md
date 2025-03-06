<svg xmlns="http://www.w3.org/2000/svg" width="500" height="500" viewBox="0 0 500 500">
  <!-- Background -->
  <rect width="500" height="500" fill="black" />

  <!-- Define gradients and filters -->
  <defs>
    <!-- Gold radial gradient for a premium metallic feel -->
    <radialGradient id="goldGradient" cx="50%" cy="50%" r="50%">
      <stop offset="0%" stop-color="#FFD700" />
      <stop offset="100%" stop-color="#B8860B" />
    </radialGradient>

    <!-- Emboss filter to add subtle shine and depth -->
    <filter id="emboss" x="-150%" y="-150%" width="400%" height="400%">
      <feGaussianBlur in="SourceAlpha" stdDeviation="2" result="blur" />
      <feOffset in="blur" dx="2" dy="2" result="offsetBlur" />
      <feSpecularLighting in="blur" surfaceScale="2" specularConstant="0.5" specularExponent="20" lighting-color="white" result="specOut">
        <fePointLight x="-5000" y="-10000" z="20000"/>
      </feSpecularLighting>
      <feComposite in="specOut" in2="SourceAlpha" operator="in" result="specOut" />
      <feComposite in="SourceGraphic" in2="specOut" operator="arithmetic" k1="0" k2="1" k3="1" k4="0"/>
    </filter>
  </defs>

  <!-- Luxora Watch Emblem (Abstract Watch Dial) -->
  <circle cx="250" cy="180" r="80" fill="url(#goldGradient)" stroke="#FFD700" stroke-width="3" filter="url(#emboss)" />

  <!-- Minimalist Clock Hands -->
  <!-- Vertical hand (pointing upward) -->
  <line x1="250" y1="180" x2="250" y2="120" stroke="black" stroke-width="5" stroke-linecap="round" filter="url(#emboss)" />
  <!-- Horizontal hand (pointing right) -->
  <line x1="250" y1="180" x2="300" y2="180" stroke="black" stroke-width="5" stroke-linecap="round" filter="url(#emboss)" />
  
  <!-- Central pivot -->
  <circle cx="250" cy="180" r="5" fill="black" />

  <!-- Brand Name "LUXORA" -->
  <text x="250" y="380" text-anchor="middle" fill="#FFD700" font-size="64" font-family="Georgia, serif" font-weight="bold" filter="url(#emboss)">
    LUXORA
  </text>
</svg>
