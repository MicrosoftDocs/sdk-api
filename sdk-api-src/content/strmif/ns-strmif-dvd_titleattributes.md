---
UID: NS:strmif.tagDVD_TitleMainAttributes
title: DVD_TitleAttributes (strmif.h)
author: windows-sdk-content
description: The DVD_TitleAttributes structure contains information about a DVD title.
old-location: dshow\dvd_titleattributes.htm
tech.root: DirectShow
ms.assetid: e80baf09-93b7-4285-ac9a-af72cae137de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DVD_TitleAttributes, DVD_TitleAttributes structure [DirectShow], DVD_TitleAttributesStructure, dshow.dvd_titleattributes, strmif/DVD_TitleAttributes
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_TitleAttributes
product: Windows
targetos: Windows
req.typenames: DVD_TitleAttributes
req.redist: 
---

# DVD_TitleAttributes structure


## -description


The <b>DVD_TitleAttributes</b> structure contains information about a DVD title.


## -struct-fields




### -field AppMode

A variable of type <a href="https://msdn.microsoft.com/f0a12b00-89a5-4b70-9a78-519ae36d1bac">DVD_TITLE_APPMODE</a> indicating whether the Navigator is in karaoke mode.
          


### -field TitleLength

A <a href="https://msdn.microsoft.com/8f2990f6-a8f5-4b16-ae30-d51ea55496ea">DVD_HMSF_TIMECODE</a> structure.


### -field VideoAttributes

A <a href="https://msdn.microsoft.com/b395a322-d63e-41a0-b97a-88f99aeba0e5">DVD_VideoAttributes</a> structure containing information about the "main" video of the current menu or title.
          


### -field ulNumberOfAudioStreams

The number of audio streams available in the title.
          


### -field AudioAttributes

An array of <a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a> structures containing information about each available audio stream in the current title.
          


### -field MultichannelAudioAttributes

An array of <a href="https://msdn.microsoft.com/8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d">DVD_MultichannelAudioAttributes</a> structures containing additional information about any available audio stream that is in a multichannel format. This structure will be filled in for the corresponding audio stream if the multichannel bit is set in that stream's <a href="https://msdn.microsoft.com/a4365c05-718e-4d48-bb2c-a13a609df82f">DVD_AudioAttributes</a> structure.
          


### -field ulNumberOfSubpictureStreams

The number of subpicture streams available in the title.
          


### -field SubpictureAttributes

An array of <a href="https://msdn.microsoft.com/55ddfa21-5600-4aa9-b554-7ff7f3c05b91">DVD_SubpictureAttributes</a> structures that contain information about each available subpicture stream in the title.
          


## -remarks



By default, the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> uses the <b>AppMode</b> member of the anonymous union to report  the title mode.

If the application sets the <b>DVD_EnableTitleLength</b> option to <b>TRUE</b>, the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> uses the <b>TitleLength</b> member of the union to report the title length. To set this option, call the <a href="https://msdn.microsoft.com/b3b28da8-b0cb-4d76-8184-93572e4b6d06">IDvdControl2::SetOption</a>method.




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/4e901e14-9e98-4ca5-ae37-7a4564b187ab">IDvdInfo2::GetTitleAttributes</a>
 

 

