# CFB Wallpaper Schedules
*from /u/infinitempg*

This project involves CSV files, Microsoft Excel, Visual Basic, and Adobe Photoshop. This involves lots of manual work as well as macro usage - and I wasn't smart enough to write down everything last year so this is an attempt to both redo a lot of the Photoshop work as well as saving it for next year.

Schedule data is generated by [Massey Ratings](http://masseyratings.com).

There are a few steps to completing this:

1. Converting the raw text from Massey Ratings to a CSV file
2. Working in Excel to make it a CSV file that is readable by Photoshop
3. Using Photoshop macros to mass-produce wallpapers

## Obtaining Schedule Data

[Here](https://www.masseyratings.com/scores.php?s=300937&sub=11604&all=1&mode=3&sch=on&format=0) is a quick link to the raw text schedule from Massey Ratings. I copied the raw text into a text editor such as TextEdit, and replaced the spaces in the raw text with commas, as well as deleting the @ and Sch portions. I also changed the dates into a format that wouldn't confuse Excel. Could I have done this by saving it as a TSV and then importing it? Probably. But it's too late now.

Afterwards, I opened this CSV in Excel and inserted **H**, **A**, and **N** location labels by making the left column away and the right column home, and then manually changing some to neutral based on if there was a location label to the right of the row. This file was then saved as a CSV that will be imported into Microsoft Excel.

## Converting to a format readable by Photoshop

I imported (copied and pasted) the data in the CSV into an Excel file with some Visual Basic code. The basic gist of it is that it gathers the schedule for each individual FBS team (a list of which is generated from the home teams on the schedule, a formula I seem to have lost), organizes it into individual lines, and then adds file paths to the logos for both the team in question as well as its opponents. The VBA file is included with the Excel file, just be sure to enable the Developer ribbon in Excel. I then exported the generated file (as well as one for teams who play 13 games seriously why is this a thing) as a CSV which can then be imported into Photoshop. Make sure that you save it as an MS-DOS type CSV, or else Photoshop will have trouble reading the characters.

## Working in Photoshop

So step one is to make sure that your CSVs work in Photoshop. In order to do this, you need to go to `Image → Variables → Data Sets` and import your CSV. Ensure that both checkboxes are checked. You should now be able to preview all of the teams.

*(Note: I'm skipping over all of the annoying variable defining because oh god that's annoying and I'm not doing that again)*

Now that your data sets play nice with Photoshop, it's time to export them into their own files. Go to `File → Export → Data Sets As Files`, and export them with the proper names and to the proper directories. This will take a long ass time and a lot of space on your scratch disk, so make sure you have that space.

Afterwards, you can import the Photoshop Actions file. This allows you to make the perspective shift and the translucency of the logos for all of the files. Go into `File → Automate → Batch` and select the `CFB Wallpapers → Merge/Perspective` action (appropriate for the aspect ratio), and then run the automation. It should poop out all of the PNG files into an `/Images` folder.

Boom, you're done! Now hope and pray that you post this at the point of maximum karma or your post will be buried into oblivion.
