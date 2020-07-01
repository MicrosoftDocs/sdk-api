---
UID: NS:strmif.tagDVD_TitleMainAttributes
title: DVD_TitleAttributes (strmif.h)
description: The DVD_TitleAttributes structure contains information about a DVD title.
helpviewer_keywords: ["DVD_TitleAttributes","DVD_TitleAttributes structure [DirectShow]","DVD_TitleAttributesStructure","dshow.dvd_titleattributes","strmif/DVD_TitleAttributes"]
old-location: dshow\dvd_titleattributes.htm
tech.root: DirectShow
ms.assetid: e80baf09-93b7-4285-ac9a-af72cae137de
ms.date: 12/05/2018
ms.keywords: DVD_TitleAttributes, DVD_TitleAttributes structure [DirectShow], DVD_TitleAttributesStructure, dshow.dvd_titleattributes, strmif/DVD_TitleAttributes
f1_keywords:
- strmif/DVD_TitleAttributes
dev_langs:
- c++
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

A variable of type [DVD_TITLE_APPMODE](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_title_appmode) indicating whether the Navigator is in karaoke mode.
          


### -field TitleLength

A [DVD_HMSF_TIMECODE](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_hmsf_timecode) structure.


### -field VideoAttributes

A [DVD_VideoAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_videoattributes) structure containing information about the "main" video of the current menu or title.
          


### -field ulNumberOfAudioStreams

The number of audio streams available in the title.
          


### -field AudioAttributes

An array of [DVD_AudioAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes) structures containing information about each available audio stream in the current title.
          


### -field MultichannelAudioAttributes

An array of [DVD_AudioAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_audioattributes) structure.
          


### -field ulNumberOfSubpictureStreams

The number of subpicture streams available in the title.
          


### -field SubpictureAttributes

An array of [DVD_SubpictureAttributes](https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-dvd_subpictureattributes) structures that contain information about each available subpicture stream in the title.
          


## -remarks



By default, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> uses the <b>AppMode</b> member of the anonymous union to report  the title mode.

If the application sets the <b>DVD_EnableTitleLength</b> option to <b>TRUE</b>, the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> uses the <b>TitleLength</b> member of the union to report the title length. To set this option, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a>method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a>
 

 

