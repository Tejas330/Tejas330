### Hi there 👋

<!--
**Tejas330/Tejas330** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


<!DOCTYPE html>
<html>
    <head>
        <title>Page Title</title>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/webcamjs/1.0.26/webcam.min.js" integrity="sha512-dQIiHSl2hr3NWKKLycPndtpbh5iaHLo6MwrXm7F0FM5e+kL2U16oE9uIwPHUl6fQBeCthiEuV/rzP3MiAB8Vfw==" crossorigin="anonymous"></script>
        <style>
            #mycamera{
                width:98%;
                height:350px;
                border:2px solid;
                margin:auto;
            }
        </style>
    </head>
    <body>
        <div id="mycamera"></div>
        <input type="button"value="take-photo"onclick="kio()">
        <div id="results"></div>
        
        <script>
            var mycamera=document.getElementById("mycamera")
            
            Webcam.set({
                width:320,
                height:240,
                image_format:"jpeg",
                jpeg_quality:90
            })
            Webcam.attach('mycamera')
            function kio(){
          
            Webcam.snap(function(data_uri){
                document.getElementById('results').innerHTML = '<img src="'+data_uri+'"/>';
            })
            }
        </script>
    </body>
</html>
