# PurgeCrapContent (pcc.exe)
A file mover that takes one argument, a text file with definitions of content you want moved.

**Syntax: pcc.exe text.txt**
  
  This will start scanning .bin files for any defined lines in the text.txt
  file and if a match is found, the file will be moved to a subfolder (2delete)
  that is automatically created each time the program starts.
  
The definition text file is just a standard text file with a definition on each line like:

  <html>
  <span>
  <body>
  Bandwidth Limit Exceeded
  Account Suspended
  Page not found

One definition on each line, no spaces before or after as they would be part of the definition.

The example above would identify HTML content in the scanned .bin files and move them, once that is done
you can navigate to the subfolder and process the content further, or delete the content. I use this myself
to identify HTML content, separate it and get rid of it and other unwanted formats when scraping for malware.

You can also identify specific file formats by using common tags in the file

  minor_version = MP3 files
  u?fI          = WMA files
  WAVEfmt       = Wav files
  IHDR          = PNG files
  GIF87a        = GIF files

This would find and move those files into the subfolder to separate them from the content you want to focus on.
