---
UID: NE:strmif.DVD_TextStringType
title: DVD_TextStringType
author: windows-driver-content
description: Defines a subset of the DVD text-string types.
old-location: dshow\dvd_textstringtype.htm
old-project: DirectShow
ms.assetid: e8308432-a9a1-40d5-abec-aa6f86af9e5b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: DVD_Channel_Audio, DVD_General_Comments, DVD_General_Name, DVD_Other_Cut, DVD_Other_Scene, DVD_Other_Take, DVD_Stream_Angle, DVD_Stream_Audio, DVD_Stream_Subpicture, DVD_Struct_Cell, DVD_Struct_ParentalID, DVD_Struct_PartOfTitle, DVD_Struct_Title, DVD_Struct_Volume, DVD_TextStringType, DVD_TextStringType , DVD_TextStringType enumeration [DirectShow], DVD_TextStringTypeEnumeration, DVD_Title_Album, DVD_Title_Movie, DVD_Title_Orig_Album, DVD_Title_Orig_Movie, DVD_Title_Orig_Other, DVD_Title_Orig_Series, DVD_Title_Orig_Song, DVD_Title_Orig_Video, DVD_Title_Other, DVD_Title_Series, DVD_Title_Song, DVD_Title_Sub_Album, DVD_Title_Sub_Movie, DVD_Title_Sub_Other, DVD_Title_Sub_Series, DVD_Title_Sub_Song, DVD_Title_Sub_Video, DVD_Title_Video, _DVD_TextStringType, dshow.dvd_textstringtype, strmif/DVD_Channel_Audio, strmif/DVD_General_Comments, strmif/DVD_General_Name, strmif/DVD_Other_Cut, strmif/DVD_Other_Scene, strmif/DVD_Other_Take, strmif/DVD_Stream_Angle, strmif/DVD_Stream_Audio, strmif/DVD_Stream_Subpicture, strmif/DVD_Struct_Cell, strmif/DVD_Struct_ParentalID, strmif/DVD_Struct_PartOfTitle, strmif/DVD_Struct_Title, strmif/DVD_Struct_Volume, strmif/DVD_TextStringType, strmif/DVD_Title_Album, strmif/DVD_Title_Movie, strmif/DVD_Title_Orig_Album, strmif/DVD_Title_Orig_Movie, strmif/DVD_Title_Orig_Other, strmif/DVD_Title_Orig_Series, strmif/DVD_Title_Orig_Song, strmif/DVD_Title_Orig_Video, strmif/DVD_Title_Other, strmif/DVD_Title_Series, strmif/DVD_Title_Song, strmif/DVD_Title_Sub_Album, strmif/DVD_Title_Sub_Movie, strmif/DVD_Title_Sub_Other, strmif/DVD_Title_Sub_Series, strmif/DVD_Title_Sub_Song, strmif/DVD_Title_Sub_Video, strmif/DVD_Title_Video
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_TextStringType
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# DVD_TextStringType enumeration


## -description



Defines a subset of the DVD text-string types.




## -enum-fields




### -field DVD_Struct_Volume


            Indicates the top-level of the logical hierarchy. Refers to the entire contents of a one-sided disc or one side of a two-sided disc.
          


### -field DVD_Struct_Title


            Indicates that all content strings, until the next <b>DVD_Struct_Title</b>, belong to one title.
          


### -field DVD_Struct_ParentalID


            Indicates the parental ID of the following strings.
          


### -field DVD_Struct_PartOfTitle


            Indicates that all content strings, until the next <b>DVD_Struct_PartOfTitle</b>, belong to one chapter.
          


### -field DVD_Struct_Cell

Indicates that all content strings, until the next <b>DVD_Struct_Cell</b>, belong to one cell, which can be a scene from a chapter.


### -field DVD_Stream_Audio


            Indicates that the following content strings refer to the audio stream.
          


### -field DVD_Stream_Subpicture


            Indicates that the following content strings refer to the subpicture stream.
          


### -field DVD_Stream_Angle


            Indicates that the following content strings refer to the angle.
          


### -field DVD_Channel_Audio


            Indicates that the following content strings refer to the audio channel.
          


### -field DVD_General_Name


            Indicates the most important content string. Strings of this type contain the name of the volume, title, chapter, and so on, and can follow any structure identifiers.
          


### -field DVD_General_Comments


            Identifies a content string with additional information about the title, chapter, and so on, described by the <b>DVD_General_Name</b> string. The exact nature or structure of these comments is not defined.
          


### -field DVD_Title_Series


            Identifies a content string containing the name of a series to which the title belongs.
          


### -field DVD_Title_Movie


            Identifies a content string with the main movie title.
          


### -field DVD_Title_Video


            Identifies a content string containing the name of the video title.
          


### -field DVD_Title_Album


            Identifies a content string containing the name of the album title.
          


### -field DVD_Title_Song


            Identifies a content string containing the name of the song title.
          


### -field DVD_Title_Other


            Identifies a content string containing the name of the title of some other genre.
          


### -field DVD_Title_Sub_Series


            Identifies a content string with the name of the series localized to a particular country/region.
          


### -field DVD_Title_Sub_Movie


            Identifies a content string with the movie title localized to a particular country/region.
          


### -field DVD_Title_Sub_Video


            Identifies a content string with the video title localized to a particular country/region.
          


### -field DVD_Title_Sub_Album


            Identifies a content string with the album title localized to a particular country/region.
          


### -field DVD_Title_Sub_Song


            Identifies a content string with the song title localized to a particular country/region.
          


### -field DVD_Title_Sub_Other


            Identifies a content string with the title of some other genre localized to a particular country/region.
          


### -field DVD_Title_Orig_Series


            Identifies a content string with the original name of the series.
          


### -field DVD_Title_Orig_Movie


            Identifies a content string with the original name of the movie.
          


### -field DVD_Title_Orig_Video


            Identifies a content string with the original name of the video.
          


### -field DVD_Title_Orig_Album


            Identifies a content string with the original name of the album.
          


### -field DVD_Title_Orig_Song


            Identifies a content string with the original name of the song.
          


### -field DVD_Title_Orig_Other


            Identifies a content string with the original name of the content.
          


### -field DVD_Other_Scene


            Identifies a content string pertaining to a particular scene in a movie or video.
          


### -field DVD_Other_Cut


            Identifies a content string pertaining to a particular cut in a movie or video.
          


### -field DVD_Other_Take


            Identifies a content string pertaining to a particular take in a movie or video.
          


## -remarks



The <a href="https://msdn.microsoft.com/e13d4212-0e4a-40cf-89c7-f0c22f5a5cb9">IDvdInfo2::GetDVDTextStringAsUnicode</a> and <a href="https://msdn.microsoft.com/a162b4ad-28f2-49fc-9b32-72538be9ddd5">IDvdInfo2::GetDVDTextStringAsNative</a> methods return this enumeration type. The value specifies how the text string is categorized. These methods can also return identifiers that are not defined in this enumeration. For more information, see <a href="https://msdn.microsoft.com/6d415ebb-5cd0-4631-9404-f2ebabef2476">Working with DVD Text Strings</a>.

Not every DVD text string identifier is included in this enumeration, so an authored DVD might include other values.

One important identifier that is not included in this enumeration is 0xF0, the code for sorting. You can use this string to sort the string data. It can be a unique number or a repetition of a previous string with the word order changed. For example, a DVD might have a string of 0x30 (DVD_General_Name) with the value "The Greatest Hits", which might be followed by another string of type 0xF0 with the value "Greatest Hits, The". As with content strings, however, the use of the sorting string is not strictly defined.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/6d415ebb-5cd0-4631-9404-f2ebabef2476">Working with DVD Text Strings</a>
 

 

