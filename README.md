Glitchy 3 Bit Dither
==============
Implemented by Nolan Caudill, "Enhanced" by JKircharz

<p>Originally, Nolan Caudill's demo used two different error-diffusion dithering algorithms: <a href="http://verlagmartinkoch.at/software/dither/index.html">Atkinson's</a> and the <a href="http://en.wikipedia.org/wiki/Floyd%E2%80%93Steinberg_dithering">Floyd-Steinberg</a>. Now it does more. So much more. ( Insert maniacal laughter )

<p>This runs completely client-side, using the FileReader and canvas APIs. If you have a decent browser, this could work. Also, you can right-click and save the result of the processing.</p>

The demo lives <a href="http://jkirchartz.com/Glitchy3bitdither/">here</a>.

To see some curated images check out <http://glitches.jkirchartz.com/>


## Basic Usage:

    // setup canvas
    var ctx = canvas.getContext('2d');
    // get data
    var imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
    // apply a corruption to an image
    ctx.putImageData(Glitch(imageData), 0, 0);
    var img = document.createElement('img');
    // send output to img element on the page
    img.src = canvas.toDataURL("image/png");
    document.body.appendChild(img);
