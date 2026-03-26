<div align="center">
  <style>
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    
    @keyframes slideIn {
      from { opacity: 0; transform: translateX(-30px); }
      to { opacity: 1; transform: translateX(0); }
    }
    
    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.05); }
    }
    
    .hover-header {
      transition: all 0.4s ease-in-out;
      cursor: pointer;
    }
    
    .hover-header:hover {
      opacity: 0;
      transform: translateY(-30px);
      pointer-events: none;
    }
    
    .hover-header:hover + .content-reveal {
      opacity: 1;
      transform: translateY(0);
      pointer-events: auto;
    }
    
    .content-reveal {
      opacity: 0;
      transform: translateY(-20px);
      transition: all 0.5s ease-in-out;
      pointer-events: none;
    }
    
    .social-icon {
      transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
      display: inline-block;
      margin: 0 15px;
    }
    
    .social-icon:hover {
      transform: translateY(-8px) scale(1.1);
      filter: drop-shadow(0 5px 15px rgba(0,0,0,0.3));
    }
    
    .skill-bar {
      transition: width 1s ease-in-out;
      animation: slideIn 0.8s ease-out;
    }
    
    .stat-card {
      transition: all 0.3s ease;
    }
    
    .stat-card:hover {
      transform: translateY(-5px);
      filter: drop-shadow(0 8px 20px rgba(108,99,255,0.2));
    }
    
    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }
    
    .gradient-text {
      background: linear-gradient(135deg, #FF6B6B, #4ECDC4, #FFE66D, #6C63FF);
      background-size: 300% 300%;
      animation: gradientShift 3s ease infinite;
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
  </style>
  
  <!-- HEADER WITH HOVER EFFECT - DISAPPEARS ON HOVER -->
  <div class="hover-header">
    <svg width="600" height="150" xmlns="http://www.w3.org/2000/svg">
      <defs>
        <linearGradient id="headerGrad" x1="0%" y1="0%" x2="100%" y2="0%">
          <stop offset="0%" stop-color="#FF6B6B"/>
          <stop offset="50%" stop-color="#4ECDC4"/>
          <stop offset="100%" stop-color="#6C63FF"/>
        </linearGradient>
        <filter id="glow">
          <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
          <feMerge>
            <feMergeNode in="coloredBlur"/>
            <feMergeNode in="SourceGraphic"/>
          </feMerge>
        </filter>
      </defs>
      <rect width="600" height="150" fill="url(#headerGrad)" rx="20" opacity="0.1"/>
      <text x="300" y="60" text-anchor="middle" font-family="Arial, sans-serif" font-size="48" font-weight="bold" fill="url(#headerGrad)" filter="url(#glow)">
        LOVANDRA
      </text>
      <text x="300" y="100" text-anchor="middle" font-family="Arial, sans-serif" font-size="18" fill="#888">
        hover to reveal content
      </text>
      <text x="300" y="125" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#AAA">
        ↓ move cursor here ↓
      </text>
    </svg>
  </div>
  
  <!-- CONTENT THAT APPEARS AFTER HOVER -->
  <div class="content-reveal">
    
    <!-- PROFILE INTRODUCTION -->
    <svg width="800" height="120" xmlns="http://www.w3.org/2000/svg">
      <rect width="800" height="120" fill="none" rx="15"/>
      <text x="400" y="35" text-anchor="middle" font-family="Arial, sans-serif" font-size="24" fill="#FF6B6B" font-weight="bold">
        digital architect
      </text>
      <text x="400" y="65" text-anchor="middle" font-family="Arial, sans-serif" font-size="16" fill="#4ECDC4">
        crafting responsive web experiences with precision and creativity
      </text>
      <text x="400" y="95" text-anchor="middle" font-family="Arial, sans-serif" font-size="14" fill="#AAA">
        indonesia based · 3+ years experience · 15+ projects completed
      </text>
    </svg>
    
    <br/>
    
    <!-- SKILLS SECTION WITH PERSENTASE -->
    <svg width="800" height="40" xmlns="http://www.w3.org/2000/svg">
      <text x="400" y="25" text-anchor="middle" font-family="Arial, sans-serif" font-size="28" fill="#6C63FF" font-weight="bold">
        technical stack
      </text>
    </svg>
    
    <table align="center" cellpadding="10">
      <tr>
        <td width="180" align="right">
          <svg width="120" height="35">
            <text x="0" y="22" fill="#E44D26" font-family="Arial, sans-serif" font-size="18" font-weight="bold">HTML5</text>
          </svg>
        </td>
        <td width="400">
          <svg width="400" height="35">
            <rect width="400" height="25" fill="#2D2D3A" rx="12"/>
            <rect class="skill-bar" width="160" height="25" fill="#E44D26" rx="12">
              <animate attributeName="width" from="0" to="160" dur="1s" fill="freeze"/>
            </rect>
            <text x="185" y="20" fill="white" font-family="Arial" font-size="12" font-weight="bold">40%</text>
          </svg>
        </td>
        <td width="100">
          <svg width="80" height="35">
            <text x="0" y="22" fill="#E44D26" font-family="Arial" font-size="14">advanced</text>
          </svg>
        </td>
      </tr>
      <tr>
        <td align="right">
          <svg width="120" height="35">
            <text x="0" y="22" fill="#264DE4" font-family="Arial, sans-serif" font-size="18" font-weight="bold">CSS3</text>
          </svg>
        </td>
        <td>
          <svg width="400" height="35">
            <rect width="400" height="25" fill="#2D2D3A" rx="12"/>
            <rect class="skill-bar" width="136" height="25" fill="#264DE4" rx="12">
              <animate attributeName="width" from="0" to="136" dur="1s" fill="freeze"/>
            </rect>
            <text x="161" y="20" fill="white" font-family="Arial" font-size="12">34%</text>
          </svg>
        </td>
        <td>
          <svg width="80" height="35">
            <text x="0" y="22" fill="#264DE4" font-family="Arial" font-size="14">intermediate</text>
          </svg>
        </td>
      </tr>
      <tr>
        <td align="right">
          <svg width="120" height="35">
            <text x="0" y="22" fill="#F7DF1E" font-family="Arial, sans-serif" font-size="18" font-weight="bold">JavaScript</text>
          </svg>
        </td>
        <td>
          <svg width="400" height="35">
            <rect width="400" height="25" fill="#2D2D3A" rx="12"/>
            <rect class="skill-bar" width="40" height="25" fill="#F7DF1E" rx="12">
              <animate attributeName="width" from="0" to="40" dur="1s" fill="freeze"/>
            </rect>
            <text x="65" y="20" fill="white" font-family="Arial" font-size="12">10%</text>
          </svg>
        </td>
        <td>
          <svg width="80" height="35">
            <text x="0" y="22" fill="#F7DF1E" font-family="Arial" font-size="14">beginner</text>
          </svg>
        </td>
      </tr>
      <tr>
        <td align="right">
          <svg width="120" height="35">
            <text x="0" y="22" fill="#3776AB" font-family="Arial, sans-serif" font-size="18" font-weight="bold">Python</text>
          </svg>
        </td>
        <td>
          <svg width="400" height="35">
            <rect width="400" height="25" fill="#2D2D3A" rx="12"/>
            <rect class="skill-bar" width="64" height="25" fill="#3776AB" rx="12">
              <animate attributeName="width" from="0" to="64" dur="1s" fill="freeze"/>
            </rect>
            <text x="89" y="20" fill="white" font-family="Arial" font-size="12">16%</text>
          </svg>
        </td>
        <td>
          <svg width="80" height="35">
            <text x="0" y="22" fill="#3776AB" font-family="Arial" font-size="14">learning</text>
          </svg>
        </td>
      </tr>
    </table>
    
    <br/>
    
    <!-- SOCIAL MEDIA WITH ICONS (SVG ICONS) -->
    <svg width="800" height="40" xmlns="http://www.w3.org/2000/svg">
      <text x="400" y="25" text-anchor="middle" font-family="Arial, sans-serif" font-size="28" fill="#FF8C42" font-weight="bold">
        connect with me
      </text>
    </svg>
    
    <div align="center">
      <!-- Instagram Icon -->
      <a href="https://instagram.com/chegi_lovandra" target="_blank" style="text-decoration: none;">
        <div class="social-icon">
          <svg width="90" height="90" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient id="instaGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#F58529"/>
                <stop offset="30%" stop-color="#DD2A7B"/>
                <stop offset="60%" stop-color="#8134AF"/>
                <stop offset="100%" stop-color="#515BD4"/>
              </linearGradient>
              <filter id="shadow">
                <feDropShadow dx="0" dy="4" stdDeviation="3" flood-opacity="0.3"/>
              </filter>
            </defs>
            <rect width="90" height="90" fill="url(#instaGrad)" rx="22" filter="url(#shadow)"/>
            <circle cx="45" cy="45" r="18" fill="none" stroke="white" stroke-width="3"/>
            <circle cx="45" cy="45" r="8" fill="white"/>
            <circle cx="68" cy="28" r="4" fill="white"/>
            <text x="45" y="82" text-anchor="middle" fill="white" font-family="Arial" font-size="10">INSTA</text>
          </svg>
        </div>
      </a>
      
      <!-- YouTube Icon -->
      <a href="https://youtube.com/@Lovandra-23" target="_blank" style="text-decoration: none;">
        <div class="social-icon">
          <svg width="90" height="90" xmlns="http://www.w3.org/2000/svg">
            <rect width="90" height="90" fill="#FF0000" rx="22" filter="url(#shadow)"/>
            <polygon points="60,45 38,32 38,58" fill="white"/>
            <text x="45" y="82" text-anchor="middle" fill="white" font-family="Arial" font-size="10">YOUTUBE</text>
          </svg>
        </div>
      </a>
      
      <!-- Gmail Icon -->
      <a href="mailto:lovandraweb@gmail.com" target="_blank" style="text-decoration: none;">
        <div class="social-icon">
          <svg width="90" height="90" xmlns="http://www.w3.org/2000/svg">
            <defs>
              <linearGradient id="gmailGrad" x1="0%" y1="0%" x2="100%" y2="100%">
                <stop offset="0%" stop-color="#D14836"/>
                <stop offset="100%" stop-color="#B23121"/>
              </linearGradient>
            </defs>
            <rect width="90" height="90" fill="url(#gmailGrad)" rx="22" filter="url(#shadow)"/>
            <rect x="20" y="32" width="50" height="32" fill="none" stroke="white" stroke-width="2"/>
            <polygon points="45,52 20,32 70,32" fill="white"/>
            <text x="45" y="82" text-anchor="middle" fill="white" font-family="Arial" font-size="10">GMAIL</text>
          </svg>
        </div>
      </a>
    </div>
    
    <div align="center">
      <svg width="300" height="25">
        <text x="150" y="17" text-anchor="middle" fill="#F58529" font-family="Arial" font-size="12">@chegi_lovandra</text>
      </svg>
      <svg width="300" height="25">
        <text x="150" y="17" text-anchor="middle" fill="#FF0000" font-family="Arial" font-size="12">@Lovandra-23</text>
      </svg>
      <svg width="300" height="25">
        <text x="150" y="17" text-anchor="middle" fill="#D14836" font-family="Arial" font-size="12">lovandraweb@gmail.com</text>
      </svg>
    </div>
    
    <br/>
    
    <!-- STATISTICS SECTION -->
    <svg width="800" height="40" xmlns="http://www.w3.org/2000/svg">
      <text x="400" y="25" text-anchor="middle" font-family="Arial, sans-serif" font-size="28" fill="#4ECDC4" font-weight="bold">
        github insights
      </text>
    </svg>
    
    <div align="center">
      <table align="center" cellpadding="15">
        <tr>
          <td>
            <div class="stat-card">
              <svg width="180" height="120" xmlns="http://www.w3.org/2000/svg">
                <rect width="180" height="120" fill="#0D1117" rx="12" stroke="#6C63FF" stroke-width="2"/>
                <text x="90" y="45" text-anchor="middle" fill="#FF6B6B" font-family="Arial" font-size="32" font-weight="bold">24</text>
                <text x="90" y="75" text-anchor="middle" fill="#AAA" font-family="Arial" font-size="12">total repositories</text>
                <text x="90" y="95" text-anchor="middle" fill="#6C63FF" font-family="Arial" font-size="10">public contributions</text>
              </svg>
            </div>
          </td>
          <td>
            <div class="stat-card">
              <svg width="180" height="120" xmlns="http://www.w3.org/2000/svg">
                <rect width="180" height="120" fill="#0D1117" rx="12" stroke="#4ECDC4" stroke-width="2"/>
                <text x="90" y="45" text-anchor="middle" fill="#4ECDC4" font-family="Arial" font-size="32" font-weight="bold">347</text>
                <text x="90" y="75" text-anchor="middle" fill="#AAA" font-family="Arial" font-size="12">contributions</text>
                <text x="90" y="95" text-anchor="middle" fill="#4ECDC4" font-family="Arial" font-size="10">last 12 months</text>
              </svg>
            </div>
          </td>
          <td>
            <div class="stat-card">
              <svg width="180" height="120" xmlns="http://www.w3.org/2000/svg">
                <rect width="180" height="120" fill="#0D1117" rx="12" stroke="#FFE66D" stroke-width="2"/>
                <text x="90" y="45" text-anchor="middle" fill="#FFE66D" font-family="Arial" font-size="32" font-weight="bold">1.2k</text>
                <text x="90" y="75" text-anchor="middle" fill="#AAA" font-family="Arial" font-size="12">profile views</text>
                <text x="90" y="95" text-anchor="middle" fill="#FFE66D" font-family="Arial" font-size="10">total visits</text>
              </svg>
            </div>
          </td>
        </tr>
      </table>
    </div>
    
    <br/>
    
    <!-- FOOTER WITH GRADIENT TEXT -->
    <svg width="800" height="70" xmlns="http://www.w3.org/2000/svg">
      <rect width="800" height="70" fill="none"/>
      <text x="400" y="25" text-anchor="middle" font-family="Arial, sans-serif" font-size="16" class="gradient-text" font-weight="bold">
        build with intention · create with passion · ship with pride
      </text>
      <text x="400" y="55" text-anchor="middle" font-family="Arial, sans-serif" font-size="12" fill="#666">
        lovandra · 2026 · available for collaboration
      </text>
    </svg>
    
  </div>
</div>
