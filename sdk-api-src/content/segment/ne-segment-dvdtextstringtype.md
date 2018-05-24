---
UID: NE:segment.DVDTextStringType
title: DVDTextStringType
author: windows-driver-content
description: The DVDTextStringType enumeration type indicates the type of information contained in a DVD text string.
old-location: mstv\dvdtextstringtype.htm
old-project: mstv
ms.assetid: 4ed4d0a5-31f1-418a-a0c9-c6f4997ef63b
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: DVDTextStringType, DVDTextStringType enumeration [Microsoft TV Technologies], dvdChannel_Audio, dvdGeneral_Comments, dvdGeneral_Name, dvdOther_Cut, dvdOther_Scene, dvdOther_Take, dvdStream_Angle, dvdStream_Audio, dvdStream_Subpicture, dvdStruct_Cell, dvdStruct_ParentalID, dvdStruct_PartOfTitle, dvdStruct_Title, dvdStruct_Volume, dvdTitle_Album, dvdTitle_Movie, dvdTitle_Orig_Album, dvdTitle_Orig_Movie, dvdTitle_Orig_Other, dvdTitle_Orig_Series, dvdTitle_Orig_Song, dvdTitle_Orig_Video, dvdTitle_Other, dvdTitle_Series, dvdTitle_Song, dvdTitle_Sub_Album, dvdTitle_Sub_Movie, dvdTitle_Sub_Other, dvdTitle_Sub_Series, dvdTitle_Sub_Song, dvdTitle_Sub_Video, dvdTitle_Video, mstv.dvdtextstringtype, segment/DVDTextStringType, segment/dvdChannel_Audio, segment/dvdGeneral_Comments, segment/dvdGeneral_Name, segment/dvdOther_Cut, segment/dvdOther_Scene, segment/dvdOther_Take, segment/dvdStream_Angle, segment/dvdStream_Audio, segment/dvdStream_Subpicture, segment/dvdStruct_Cell, segment/dvdStruct_ParentalID, segment/dvdStruct_PartOfTitle, segment/dvdStruct_Title, segment/dvdStruct_Volume, segment/dvdTitle_Album, segment/dvdTitle_Movie, segment/dvdTitle_Orig_Album, segment/dvdTitle_Orig_Movie, segment/dvdTitle_Orig_Other, segment/dvdTitle_Orig_Series, segment/dvdTitle_Orig_Song, segment/dvdTitle_Orig_Video, segment/dvdTitle_Other, segment/dvdTitle_Series, segment/dvdTitle_Song, segment/dvdTitle_Sub_Album, segment/dvdTitle_Sub_Movie, segment/dvdTitle_Sub_Other, segment/dvdTitle_Sub_Series, segment/dvdTitle_Sub_Song, segment/dvdTitle_Sub_Video, segment/dvdTitle_Video
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: segment.h
req.include-header: DShow.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DVDTextStringType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	segment.h
api_name:
-	DVDTextStringType
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

