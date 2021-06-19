<html>
  <body>
    <script>
      (async () => {
        const response = await fetch('https://github.com/Tracking-the-trackers/Tracking-the-trackers.github.io/tree/main/PDFs/');
        const data = await response.json();
        let htmlString = '<ul>';
        for (let file of data) {
          htmlString += `<li><a href="${file.path}">${file.name}</a></li>`;
        }
        htmlString += '</ul>';
        document.getElementsByTagName('body')[0].innerHTML = htmlString;
      })()
    </script>
  <body>
</html>