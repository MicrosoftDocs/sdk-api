---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DVDTextStringType enumeration


## -description



The <b>DVDTextStringType</b> enumeration type indicates the type of information contained in a DVD text string.




## -enum-fields




### -field dvdStruct_Volume

Indicates the top level of the logical hierarchy. Refers to the entire contents of a one-sided disc or one side of a two-sided disc. 


### -field dvdStruct_Title

Indicates that all content strings, until the next dvd_Struct_Title, belong to one title.


### -field dvdStruct_ParentalID

Indicates the parental ID of the following strings.


### -field dvdStruct_PartOfTitle

Indicates that all content strings, until the next dvd_Struct_PartOfTitle, belong to one chapter.


### -field dvdStruct_Cell

Indicates that all content strings, until the next dvd_Struct_Cell, belong to one cell, which can be a scene from a chapter.


### -field dvdStream_Audio

Indicates that the following content strings refer to the audio stream.


### -field dvdStream_Subpicture

Indicates that the following content strings refer to the subpicture stream.


### -field dvdStream_Angle

Indicates that the following content strings refer to the angle.


### -field dvdChannel_Audio

Indicates that the following content strings refer to the audio channel.


### -field dvdGeneral_Name

Indicates the most important content string. Strings of this type contain the name of the volume, title, chapter, and so on, and can follow any structure identifiers.


### -field dvdGeneral_Comments

Identifies a content string with additional information about the title, chapter, and so on, described by the dvd_General_Name string. The exact nature or structure of these comments is not defined.


### -field dvdTitle_Series

Identifies a content string containing the name of a series to which the title belongs.


### -field dvdTitle_Movie

Identifies a content string with the main movie title.


### -field dvdTitle_Video

Identifies a content string containing the name of the video title.


### -field dvdTitle_Album

Identifies a content string containing the name of the album title.


### -field dvdTitle_Song

Identifies a content string containing the name of the song title.


### -field dvdTitle_Other

Identifies a content string containing the name of the title of some other genre.


### -field dvdTitle_Sub_Series

Identifies a content string with the name of the series localized to a particular country/region.


### -field dvdTitle_Sub_Movie

Identifies a content string with the movie title localized to a particular country/region.


### -field dvdTitle_Sub_Video

Identifies a content string with the video title localized to a particular country/region.


### -field dvdTitle_Sub_Album

Identifies a content string with the album title localized to a particular country/region.


### -field dvdTitle_Sub_Song

Identifies a content string with the song title localized to a particular country/region.


### -field dvdTitle_Sub_Other

Identifies a content string with the title of some other genre localized to a particular country/region.


### -field dvdTitle_Orig_Series

Identifies a content string with the original name of the series.


### -field dvdTitle_Orig_Movie

Identifies a content string with the original name of the movie.


### -field dvdTitle_Orig_Video

Identifies a content string with the original name of the video.


### -field dvdTitle_Orig_Album

Identifies a content string with the original name of the album.


### -field dvdTitle_Orig_Song

Identifies a content string with the original name of the song.


### -field dvdTitle_Orig_Other

Identifies a content string with the original name of the content.


### -field dvdOther_Scene

Identifies a content string pertaining to a particular scene in a movie or video.


### -field dvdOther_Cut

Identifies a content string pertaining to a particular cut in a movie or video.


### -field dvdOther_Take

Identifies a content string pertaining to a particular take in a movie or video.


## -remarks



A <a href="https://msdn.microsoft.com/e8308432-a9a1-40d5-abec-aa6f86af9e5b">DVD_TextStringType</a> value is returned in the <a href="mstv.msvidwebdvd_dvdtextstringtype_property">DVDTextStringType</a> method to identify how the disc authors have categorized the specified text string. 

Not every DVD text string identifier is included in this enumeration, so an authored DVD might include other values.

One important text string type not defined in this enumeration is 0xF0, the extension-sorting text string type. You can use this type of string in many ways to enable players to sort the string data. It can be a unique number or a repetition of a previous string with the word order changed. For example, a string of type 0x30 that has the name "The Greatest Hits" might be followed by a string of type 0xF0 that says "Greatest Hits, The." As with content strings, the use of the sorting string is not strictly defined.




## -see-also




<a href="mstv.msvidwebdvd_dvdtextstringtype_property">DVDTextStringType</a>



<a href="https://msdn.microsoft.com/3c21f2c6-8eff-4fe5-a383-057f3394d9ee">Video Control Enumerations</a>



<a href="dshow.working_with_dvd_text_strings_COLLISION525">Working with DVD Text Strings</a>
 

 

