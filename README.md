<h1> The getUserMedia API </h1>
The API itself is quite simple to use, you simply ask the browser to obtain a connection to the user’s webcam (with the user’s permission of course!) and you either get the connection or you don’t.
<xmp>
navigator.getUserMedia = (navigator.getUserMedia ||
					  navigator.webkitGetUserMedia ||
					  navigator.mozGetUserMedia ||
					  navigator.msGetUserMedia);
if (navigator.getUserMedia) {
  navigator.getUserMedia(
	 {
		video:true,
		audio:false
	 },       
	 function(stream) { /* do something */ },
	 function(error) { /* do something */ }
  );
}
else {
  alert('Sorry, the browser you are using doesn\'t support getUserMedia');
  return;
}
</xmp>
<a href="https://w3c.github.io/mediacapture-main/getusermedia.html">API LINK</a>
