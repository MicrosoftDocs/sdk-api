---
UID: NS:strmif.tagDVD_TitleMainAttributes
title: DVD_TitleAttributes (strmif.h)
author: windows-sdk-content
description: The DVD_TitleAttributes structure contains information about a DVD title.
old-location: dshow\dvd_titleattributes.htm
tech.root: DirectShow
ms.assetid: e80baf09-93b7-4285-ac9a-af72cae137de
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# DVD_TitleAttributes structure


## -description


The <b>DVD_TitleAttributes</b> structure contains information about a DVD title.


## -struct-fields




### -field AppMode

A variable of type <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_title_appmode">DVD_TITLE_APPMODE</a> indicating whether the Navigator is in karaoke mode.
          


### -field TitleLength

A <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_hmsf_timecode">DVD_HMSF_TIMECODE</a> structure.


### -field VideoAttributes

A <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_videoattributes">DVD_VideoAttributes</a> structure containing information about the "main" video of the current menu or title.
          


### -field ulNumberOfAudioStreams

The number of audio streams available in the title.
          


### -field AudioAttributes

An array of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_audioattributes">DVD_AudioAttributes</a> structures containing information about each available audio stream in the current title.
          


### -field MultichannelAudioAttributes

An array of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_multichannelaudioattributes">DVD_MultichannelAudioAttributes</a> structures containing additional information about any available audio stream that is in a multichannel format. This structure will be filled in for the corresponding audio stream if the multichannel bit is set in that stream's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_audioattributes">DVD_AudioAttributes</a> structure.
          


### -field ulNumberOfSubpictureStreams

The number of subpicture streams available in the title.
          


### -field SubpictureAttributes

An array of <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_subpictureattributes">DVD_SubpictureAttributes</a> structures that contain information about each available subpicture stream in the title.
          


## -remarks



By default, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> uses the <b>AppMode</b> member of the anonymous union to report  the title mode.

If the application sets the <b>DVD_EnableTitleLength</b> option to <b>TRUE</b>, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> uses the <b>TitleLength</b> member of the union to report the title length. To set this option, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a>method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a>
 

 

