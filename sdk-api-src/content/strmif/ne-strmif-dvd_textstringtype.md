---
UID: NE:strmif.DVD_TextStringType
title: DVD_TextStringType (strmif.h)
description: Defines a subset of the DVD text-string types.
helpviewer_keywords: ["DVD_Channel_Audio","DVD_General_Comments","DVD_General_Name","DVD_Other_Cut","DVD_Other_Scene","DVD_Other_Take","DVD_Stream_Angle","DVD_Stream_Audio","DVD_Stream_Subpicture","DVD_Struct_Cell","DVD_Struct_ParentalID","DVD_Struct_PartOfTitle","DVD_Struct_Title","DVD_Struct_Volume","DVD_TextStringType","DVD_TextStringType","DVD_TextStringType enumeration [DirectShow]","DVD_TextStringTypeEnumeration","DVD_Title_Album","DVD_Title_Movie","DVD_Title_Orig_Album","DVD_Title_Orig_Movie","DVD_Title_Orig_Other","DVD_Title_Orig_Series","DVD_Title_Orig_Song","DVD_Title_Orig_Video","DVD_Title_Other","DVD_Title_Series","DVD_Title_Song","DVD_Title_Sub_Album","DVD_Title_Sub_Movie","DVD_Title_Sub_Other","DVD_Title_Sub_Series","DVD_Title_Sub_Song","DVD_Title_Sub_Video","DVD_Title_Video","_DVD_TextStringType","dshow.dvd_textstringtype","strmif/DVD_Channel_Audio","strmif/DVD_General_Comments","strmif/DVD_General_Name","strmif/DVD_Other_Cut","strmif/DVD_Other_Scene","strmif/DVD_Other_Take","strmif/DVD_Stream_Angle","strmif/DVD_Stream_Audio","strmif/DVD_Stream_Subpicture","strmif/DVD_Struct_Cell","strmif/DVD_Struct_ParentalID","strmif/DVD_Struct_PartOfTitle","strmif/DVD_Struct_Title","strmif/DVD_Struct_Volume","strmif/DVD_TextStringType","strmif/DVD_Title_Album","strmif/DVD_Title_Movie","strmif/DVD_Title_Orig_Album","strmif/DVD_Title_Orig_Movie","strmif/DVD_Title_Orig_Other","strmif/DVD_Title_Orig_Series","strmif/DVD_Title_Orig_Song","strmif/DVD_Title_Orig_Video","strmif/DVD_Title_Other","strmif/DVD_Title_Series","strmif/DVD_Title_Song","strmif/DVD_Title_Sub_Album","strmif/DVD_Title_Sub_Movie","strmif/DVD_Title_Sub_Other","strmif/DVD_Title_Sub_Series","strmif/DVD_Title_Sub_Song","strmif/DVD_Title_Sub_Video","strmif/DVD_Title_Video"]
old-location: dshow\dvd_textstringtype.htm
tech.root: dshow
ms.assetid: e8308432-a9a1-40d5-abec-aa6f86af9e5b
ms.date: 12/05/2018
ms.keywords: DVD_Channel_Audio, DVD_General_Comments, DVD_General_Name, DVD_Other_Cut, DVD_Other_Scene, DVD_Other_Take, DVD_Stream_Angle, DVD_Stream_Audio, DVD_Stream_Subpicture, DVD_Struct_Cell, DVD_Struct_ParentalID, DVD_Struct_PartOfTitle, DVD_Struct_Title, DVD_Struct_Volume, DVD_TextStringType, DVD_TextStringType , DVD_TextStringType enumeration [DirectShow], DVD_TextStringTypeEnumeration, DVD_Title_Album, DVD_Title_Movie, DVD_Title_Orig_Album, DVD_Title_Orig_Movie, DVD_Title_Orig_Other, DVD_Title_Orig_Series, DVD_Title_Orig_Song, DVD_Title_Orig_Video, DVD_Title_Other, DVD_Title_Series, DVD_Title_Song, DVD_Title_Sub_Album, DVD_Title_Sub_Movie, DVD_Title_Sub_Other, DVD_Title_Sub_Series, DVD_Title_Sub_Song, DVD_Title_Sub_Video, DVD_Title_Video, _DVD_TextStringType, dshow.dvd_textstringtype, strmif/DVD_Channel_Audio, strmif/DVD_General_Comments, strmif/DVD_General_Name, strmif/DVD_Other_Cut, strmif/DVD_Other_Scene, strmif/DVD_Other_Take, strmif/DVD_Stream_Angle, strmif/DVD_Stream_Audio, strmif/DVD_Stream_Subpicture, strmif/DVD_Struct_Cell, strmif/DVD_Struct_ParentalID, strmif/DVD_Struct_PartOfTitle, strmif/DVD_Struct_Title, strmif/DVD_Struct_Volume, strmif/DVD_TextStringType, strmif/DVD_Title_Album, strmif/DVD_Title_Movie, strmif/DVD_Title_Orig_Album, strmif/DVD_Title_Orig_Movie, strmif/DVD_Title_Orig_Other, strmif/DVD_Title_Orig_Series, strmif/DVD_Title_Orig_Song, strmif/DVD_Title_Orig_Video, strmif/DVD_Title_Other, strmif/DVD_Title_Series, strmif/DVD_Title_Song, strmif/DVD_Title_Sub_Album, strmif/DVD_Title_Sub_Movie, strmif/DVD_Title_Sub_Other, strmif/DVD_Title_Sub_Series, strmif/DVD_Title_Sub_Song, strmif/DVD_Title_Sub_Video, strmif/DVD_Title_Video
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DVD_TextStringType
 - strmif/DVD_TextStringType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TextStringType
---

# DVD_TextStringType enumeration


## -description

Defines a subset of the DVD text-string types.

## -enum-fields

### -field DVD_Struct_Volume:0x1

Indicates the top-level of the logical hierarchy. Refers to the entire contents of a one-sided disc or one side of a two-sided disc.

### -field DVD_Struct_Title:0x2

Indicates that all content strings, until the next <b>DVD_Struct_Title</b>, belong to one title.

### -field DVD_Struct_ParentalID:0x3

Indicates the parental ID of the following strings.

### -field DVD_Struct_PartOfTitle:0x4

Indicates that all content strings, until the next <b>DVD_Struct_PartOfTitle</b>, belong to one chapter.

### -field DVD_Struct_Cell:0x5

Indicates that all content strings, until the next <b>DVD_Struct_Cell</b>, belong to one cell, which can be a scene from a chapter.

### -field DVD_Stream_Audio:0x10

Indicates that the following content strings refer to the audio stream.

### -field DVD_Stream_Subpicture:0x11

Indicates that the following content strings refer to the subpicture stream.

### -field DVD_Stream_Angle:0x12

Indicates that the following content strings refer to the angle.

### -field DVD_Channel_Audio:0x20

Indicates that the following content strings refer to the audio channel.

### -field DVD_General_Name:0x30

Indicates the most important content string. Strings of this type contain the name of the volume, title, chapter, and so on, and can follow any structure identifiers.

### -field DVD_General_Comments:0x31

Identifies a content string with additional information about the title, chapter, and so on, described by the <b>DVD_General_Name</b> string. The exact nature or structure of these comments is not defined.

### -field DVD_Title_Series:0x38

Identifies a content string containing the name of a series to which the title belongs.

### -field DVD_Title_Movie:0x39

Identifies a content string with the main movie title.

### -field DVD_Title_Video:0x3a

Identifies a content string containing the name of the video title.

### -field DVD_Title_Album:0x3b

Identifies a content string containing the name of the album title.

### -field DVD_Title_Song:0x3c

Identifies a content string containing the name of the song title.

### -field DVD_Title_Other:0x3f

Identifies a content string containing the name of the title of some other genre.

### -field DVD_Title_Sub_Series:0x40

Identifies a content string with the name of the series localized to a particular country/region.

### -field DVD_Title_Sub_Movie:0x41

Identifies a content string with the movie title localized to a particular country/region.

### -field DVD_Title_Sub_Video:0x42

Identifies a content string with the video title localized to a particular country/region.

### -field DVD_Title_Sub_Album:0x43

Identifies a content string with the album title localized to a particular country/region.

### -field DVD_Title_Sub_Song:0x44

Identifies a content string with the song title localized to a particular country/region.

### -field DVD_Title_Sub_Other:0x47

Identifies a content string with the title of some other genre localized to a particular country/region.

### -field DVD_Title_Orig_Series:0x48

Identifies a content string with the original name of the series.

### -field DVD_Title_Orig_Movie:0x49

Identifies a content string with the original name of the movie.

### -field DVD_Title_Orig_Video:0x4a

Identifies a content string with the original name of the video.

### -field DVD_Title_Orig_Album:0x4b

Identifies a content string with the original name of the album.

### -field DVD_Title_Orig_Song:0x4c

Identifies a content string with the original name of the song.

### -field DVD_Title_Orig_Other:0x4f

Identifies a content string with the original name of the content.

### -field DVD_Other_Scene:0x50

Identifies a content string pertaining to a particular scene in a movie or video.

### -field DVD_Other_Cut:0x51

Identifies a content string pertaining to a particular cut in a movie or video.

### -field DVD_Other_Take:0x52

Identifies a content string pertaining to a particular take in a movie or video.

## -remarks

The <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode">IDvdInfo2::GetDVDTextStringAsUnicode</a> and <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative">IDvdInfo2::GetDVDTextStringAsNative</a> methods return this enumeration type. The value specifies how the text string is categorized. These methods can also return identifiers that are not defined in this enumeration. For more information, see <a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>.

Not every DVD text string identifier is included in this enumeration, so an authored DVD might include other values.

One important identifier that is not included in this enumeration is 0xF0, the code for sorting. You can use this string to sort the string data. It can be a unique number or a repetition of a previous string with the word order changed. For example, a DVD might have a string of 0x30 (DVD_General_Name) with the value "The Greatest Hits", which might be followed by another string of type 0xF0 with the value "Greatest Hits, The". As with content strings, however, the use of the sorting string is not strictly defined.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/DirectShow/working-with-dvd-text-strings">Working with DVD Text Strings</a>
