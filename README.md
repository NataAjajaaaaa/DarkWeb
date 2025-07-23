<!DOCTYPE html>
<html>
<head>
  <title>Hacker Mode</title>
  <style>
    body {
      background-color: black;
      color: #00ff00;
      font-family: 'Courier New', monospace;
      padding: 20px;
      white-space: pre-wrap;
      font-size: 14px;
    }
    .cursor {
      display: inline-block;
      width: 10px;
      background: #00ff00;
      animation: blink 0.8s infinite;
    }
    @keyframes blink {
      0% { opacity: 1; }
      50% { opacity: 0; }
      100% { opacity: 1; }
    }
  </style>
</head>
<body>
  <div id="hacker-text"></div><div class="cursor"></div>

  <script>
    const textElement = document.getElementById('hacker-text');
    const hackerWords = [
      "Connecting to secure server...",
      "Access granted.",
      "Downloading intel...",
      "Bypassing firewall...",
      "Injecting payload...",
      "Decrypting archive...",
      "root@neocities:~# sudo su",
      "Accessing confidential data...",
      "Uploading to darknet...",
      "Hacking NASA...",
      "rm -rf / --no-preserve-root",
      "Installing keylogger...",
      "Backdoor established.",
      "Sniffing packets...",
      "Tor activated...",
      "Exporting logs...",
      "Tracking location...",
      "Success: File hijacked.",
      "Overclocking GPU...",
      "Launching terminal UI...",
      "Firewall: OFF",
      "🤫 You shouldn't be here..."
    ];

    let index = 0;
    function typeNext() {
      if (index >= hackerWords.length) {
        index = 0;
      }
      const line = hackerWords[index++] + "\n";
      let charIndex = 0;

      const typeChar = () => {
        if (charIndex < line.length) {
          textElement.textContent += line.charAt(charIndex++);
          setTimeout(typeChar, 30);
        } else {
          setTimeout(typeNext, 300);
        }
      };
      typeChar();
    }

    typeNext();
  </script>
</body>
</html>
