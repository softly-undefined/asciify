![asciifyimage](https://github.com/softly-undefined/asciify/blob/main/readmeimg.png?raw=true)

ASCIIFY is an image -> .txt converter using python

The math itself can be found in the asciify.py file, but to describe it lightly depending on the size you choose a differently sized rectangle of pixels is chosen, converted to greyscale, and identified by intensity value between 0 and 255. The directory of ASCII characters is then pixelated so each character contains the same number of pixels as our rectangles in the image, and also converted to an intensity array. The project next uses euclidean distances to determine the "closest" ASCII character to that section of the image. This repeated throughout the entire image creating our final product!

The image .txt files should be viewed in an editor with equal spacing between characters, with characters being white and the background being black. For best results use Apple's built in TextEdit on dark mode, which the ASCII set included was based in.

## asciify.py
This file contains the code used by all the other files to actually do the .txt file conversion. No need to alter it, and don't run it it doesn't do anything! 
## simpleasciify.py
This is where you should start!! This file is a simple interface to get your bearings on how to use asciify and create .txt representations of images.
## plotasciify.py
This file asciifys a range of pixel_sizes identified in the file so you can see what sizes might look the best. I used it extensively in my exploration in exploration.ipynb as alongside generating this range of .txt representations it stores "accuracy" values in a .csv file, enabling me to compare the graphs of different images over a range of pixel_size values.
## video.py
This file enables you to create an asciifyed video, generating a directory of .txt files containing each frame of the input video at your designated pixel_size

# Conclusion
While the simpleasciify.py file does everything an average user could want with this kind of fun small project, there's a lot of places this work could go. In the default version I use purely euclidean distances to determine accuracy, but I left it in a way that you can easily weigh the cosine similarity into the equation (I lightly considered other evaluation techniques as well which could be implemented very easily).

It's currently set up exclusively to use a dictionary of the ASCII characters and write to a .txt file, but it wouldn't be much work to use any directory of images as the "dictionary" set (for example a friend recommended using faces of a dice) to create interesting collages. Whether I come back to it someday or someone else out there does I hope it can be of some use!

-Eric Bennett 2024
