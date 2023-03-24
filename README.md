<html>
  <head>
    <meta charset="UTF-8">
    <title>FIRST WEBSITE</title>
  </head>
  <body>
    <h1>Loadstring Generator</h1>
    <p>Enter the code you want to generate a loadstring for:</p>
    <textarea id="input" rows="10" cols="50"></textarea><br><br>
    <p>Generated Loadstring:</p>
    <textarea id="output" rows="10" cols="50" readonly></textarea><br><br>
    <button onclick="generateLoadstring()">Generate Loadstring</button>
    <button onclick="copyToClipboard()">Copy to Clipboard</button>

    <script>
      function generateLoadstring() {
        var code = document.getElementById("input").value;
        var loadstring = 'loadstring(game:HttpGet("' + code + '"))()';
        document.getElementById("output").value = loadstring;
      }

      function copyToClipboard() {
        var output = document.getElementById("output");
        output.select();
        document.execCommand("copy");
        alert("Loadstring copied to clipboard!");
      }
    </script>
  </body>
</html>
