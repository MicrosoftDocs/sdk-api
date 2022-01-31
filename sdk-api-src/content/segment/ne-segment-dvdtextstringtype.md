---
UID: NE:segment.DVDTextStringType
title: DVDTextStringType (segment.h)
description: The DVDTextStringType enumeration type indicates the type of information contained in a DVD text string.
helpviewer_keywords: ["DVDTextStringType","DVDTextStringType enumeration [Microsoft TV Technologies]","dvdChannel_Audio","dvdGeneral_Comments","dvdGeneral_Name","dvdOther_Cut","dvdOther_Scene","dvdOther_Take","dvdStream_Angle","dvdStream_Audio","dvdStream_Subpicture","dvdStruct_Cell","dvdStruct_ParentalID","dvdStruct_PartOfTitle","dvdStruct_Title","dvdStruct_Volume","dvdTitle_Album","dvdTitle_Movie","dvdTitle_Orig_Album","dvdTitle_Orig_Movie","dvdTitle_Orig_Other","dvdTitle_Orig_Series","dvdTitle_Orig_Song","dvdTitle_Orig_Video","dvdTitle_Other","dvdTitle_Series","dvdTitle_Song","dvdTitle_Sub_Album","dvdTitle_Sub_Movie","dvdTitle_Sub_Other","dvdTitle_Sub_Series","dvdTitle_Sub_Song","dvdTitle_Sub_Video","dvdTitle_Video","mstv.dvdtextstringtype","segment/DVDTextStringType","segment/dvdChannel_Audio","segment/dvdGeneral_Comments","segment/dvdGeneral_Name","segment/dvdOther_Cut","segment/dvdOther_Scene","segment/dvdOther_Take","segment/dvdStream_Angle","segment/dvdStream_Audio","segment/dvdStream_Subpicture","segment/dvdStruct_Cell","segment/dvdStruct_ParentalID","segment/dvdStruct_PartOfTitle","segment/dvdStruct_Title","segment/dvdStruct_Volume","segment/dvdTitle_Album","segment/dvdTitle_Movie","segment/dvdTitle_Orig_Album","segment/dvdTitle_Orig_Movie","segment/dvdTitle_Orig_Other","segment/dvdTitle_Orig_Series","segment/dvdTitle_Orig_Song","segment/dvdTitle_Orig_Video","segment/dvdTitle_Other","segment/dvdTitle_Series","segment/dvdTitle_Song","segment/dvdTitle_Sub_Album","segment/dvdTitle_Sub_Movie","segment/dvdTitle_Sub_Other","segment/dvdTitle_Sub_Series","segment/dvdTitle_Sub_Song","segment/dvdTitle_Sub_Video","segment/dvdTitle_Video"]
old-location: mstv\dvdtextstringtype.htm
tech.root: mstv
ms.assetid: 4ed4d0a5-31f1-418a-a0c9-c6f4997ef63b
ms.date: 12/05/2018
ms.keywords: DVDTextStringType, DVDTextStringType enumeration [Microsoft TV Technologies], dvdChannel_Audio, dvdGeneral_Comments, dvdGeneral_Name, dvdOther_Cut, dvdOther_Scene, dvdOther_Take, dvdStream_Angle, dvdStream_Audio, dvdStream_Subpicture, dvdStruct_Cell, dvdStruct_ParentalID, dvdStruct_PartOfTitle, dvdStruct_Title, dvdStruct_Volume, dvdTitle_Album, dvdTitle_Movie, dvdTitle_Orig_Album, dvdTitle_Orig_Movie, dvdTitle_Orig_Other, dvdTitle_Orig_Series, dvdTitle_Orig_Song, dvdTitle_Orig_Video, dvdTitle_Other, dvdTitle_Series, dvdTitle_Song, dvdTitle_Sub_Album, dvdTitle_Sub_Movie, dvdTitle_Sub_Other, dvdTitle_Sub_Series, dvdTitle_Sub_Song, dvdTitle_Sub_Video, dvdTitle_Video, mstv.dvdtextstringtype, segment/DVDTextStringType, segment/dvdChannel_Audio, segment/dvdGeneral_Comments, segment/dvdGeneral_Name, segment/dvdOther_Cut, segment/dvdOther_Scene, segment/dvdOther_Take, segment/dvdStream_Angle, segment/dvdStream_Audio, segment/dvdStream_Subpicture, segment/dvdStruct_Cell, segment/dvdStruct_ParentalID, segment/dvdStruct_PartOfTitle, segment/dvdStruct_Title, segment/dvdStruct_Volume, segment/dvdTitle_Album, segment/dvdTitle_Movie, segment/dvdTitle_Orig_Album, segment/dvdTitle_Orig_Movie, segment/dvdTitle_Orig_Other, segment/dvdTitle_Orig_Series, segment/dvdTitle_Orig_Song, segment/dvdTitle_Orig_Video, segment/dvdTitle_Other, segment/dvdTitle_Series, segment/dvdTitle_Song, segment/dvdTitle_Sub_Album, segment/dvdTitle_Sub_Movie, segment/dvdTitle_Sub_Other, segment/dvdTitle_Sub_Series, segment/dvdTitle_Sub_Song, segment/dvdTitle_Sub_Video, segment/dvdTitle_Video
req.header: segment.h
req.include-header: DShow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DVDTextStringType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DVDTextStringType
 - segment/DVDTextStringType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - segment.h
api_name:
 - DVDTextStringType
---

# DVDTextStringType enumeration


## -description

The <b>DVDTextStringType</b> enumeration type indicates the type of information contained in a DVD text string.

## -enum-fields

### -field dvdStruct_Volume:0x1

Indicates the top level of the logical hierarchy. Refers to the entire contents of a one-sided disc or one side of a two-sided disc.

### -field dvdStruct_Title:0x2

Indicates that all content strings, until the next dvd_Struct_Title, belong to one title.

### -field dvdStruct_ParentalID:0x3

Indicates the parental ID of the following strings.

### -field dvdStruct_PartOfTitle:0x4

Indicates that all content strings, until the next dvd_Struct_PartOfTitle, belong to one chapter.

### -field dvdStruct_Cell:0x5

Indicates that all content strings, until the next dvd_Struct_Cell, belong to one cell, which can be a scene from a chapter.

### -field dvdStream_Audio:0x10

Indicates that the following content strings refer to the audio stream.

### -field dvdStream_Subpicture:0x11

Indicates that the following content strings refer to the subpicture stream.

### -field dvdStream_Angle:0x12

Indicates that the following content strings refer to the angle.

### -field dvdChannel_Audio:0x20

Indicates that the following content strings refer to the audio channel.

### -field dvdGeneral_Name:0x30

Indicates the most important content string. Strings of this type contain the name of the volume, title, chapter, and so on, and can follow any structure identifiers.

### -field dvdGeneral_Comments:0x31

Identifies a content string with additional information about the title, chapter, and so on, described by the dvd_General_Name string. The exact nature or structure of these comments is not defined.

### -field dvdTitle_Series:0x38

Identifies a content string containing the name of a series to which the title belongs.

### -field dvdTitle_Movie:0x39

Identifies a content string with the main movie title.

### -field dvdTitle_Video:0x3a

Identifies a content string containing the name of the video title.

### -field dvdTitle_Album:0x3b

Identifies a content string containing the name of the album title.

### -field dvdTitle_Song:0x3c

Identifies a content string containing the name of the song title.

### -field dvdTitle_Other:0x3f

Identifies a content string containing the name of the title of some other genre.

### -field dvdTitle_Sub_Series:0x40

Identifies a content string with the name of the series localized to a particular country/region.

### -field dvdTitle_Sub_Movie:0x41

Identifies a content string with the movie title localized to a particular country/region.

### -field dvdTitle_Sub_Video:0x42

Identifies a content string with the video title localized to a particular country/region.

### -field dvdTitle_Sub_Album:0x43

Identifies a content string with the album title localized to a particular country/region.

### -field dvdTitle_Sub_Song:0x44

Identifies a content string with the song title localized to a particular country/region.

### -field dvdTitle_Sub_Other:0x47

Identifies a content string with the title of some other genre localized to a particular country/region.

### -field dvdTitle_Orig_Series:0x48

Identifies a content string with the original name of the series.

### -field dvdTitle_Orig_Movie:0x49

Identifies a content string with the original name of the movie.

### -field dvdTitle_Orig_Video:0x4a

Identifies a content string with the original name of the video.

### -field dvdTitle_Orig_Album:0x4b

Identifies a content string with the original name of the album.

### -field dvdTitle_Orig_Song:0x4c

Identifies a content string with the original name of the song.

### -field dvdTitle_Orig_Other:0x4f

Identifies a content string with the original name of the content.

### -field dvdOther_Scene:0x50

Identifies a content string pertaining to a particular scene in a movie or video.

### -field dvdOther_Cut:0x51

Identifies a content string pertaining to a particular cut in a movie or video.

### -field dvdOther_Take:0x52

Identifies a content string pertaining to a particular take in a movie or video.

## -remarks

A <a href="/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype">DVD_TextStringType</a> value is returned in the <a href="/windows/desktop/api/segment/ne-segment-dvdtextstringtype">DVDTextStringType</a> method to identify how the disc authors have categorized the specified text string. 

Not every DVD text string identifier is included in this enumeration, so an authored DVD might include other values.

One important text string type not defined in this enumeration is 0xF0, the extension-sorting text string type. You can use this type of string in many ways to enable players to sort the string data. It can be a unique number or a repetition of a previous string with the word order changed. For example, a string of type 0x30 that has the name "The Greatest Hits" might be followed by a string of type 0xF0 that says "Greatest Hits, The." As with content strings, the use of the sorting string is not strictly defined.

## -see-also

<a href="/windows/desktop/api/segment/ne-segment-dvdtextstringtype">DVDTextStringType</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-enumerations">Video Control Enumerations</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>
