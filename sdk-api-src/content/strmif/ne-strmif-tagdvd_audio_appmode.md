---
UID: NE:strmif.tagDVD_AUDIO_APPMODE
title: tagDVD_AUDIO_APPMODE
author: windows-sdk-content
description: Indicates the current audio mode as retrieved in a call to IDvdInfo2::GetAudioAttributes.
old-location: dshow\dvd_audio_appmode.htm
old-project: DirectShow
ms.assetid: 900fd812-7ca0-4dd8-bb30-3c8eff136939
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DVD_AUDIO_APPMODE, DVD_AUDIO_APPMODE , DVD_AUDIO_APPMODE enumeration [DirectShow], DVD_AUDIO_APPMODEEnumeration, DVD_AudioMode_Karaoke, DVD_AudioMode_None, DVD_AudioMode_Other, DVD_AudioMode_Surround, dshow.dvd_audio_appmode, strmif/DVD_AUDIO_APPMODE, strmif/DVD_AudioMode_Karaoke, strmif/DVD_AudioMode_None, strmif/DVD_AudioMode_Other, strmif/DVD_AudioMode_Surround, tagDVD_AUDIO_APPMODE
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_AUDIO_APPMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_AUDIO_APPMODE
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
---

# tagDVD_AUDIO_APPMODE enumeration


## -description



Indicates the current audio mode as retrieved in a call to <a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a>.




## -enum-fields




### -field DVD_AudioMode_None

No special audio mode. The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> will send the audio to the decoder with no special processing.
          


### -field DVD_AudioMode_Karaoke

The current audio mode is karaoke content.
          


### -field DVD_AudioMode_Surround

The current audio mode is surround sound.
          


### -field DVD_AudioMode_Other

Unrecognized audio mode.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/80291efa-f3eb-47f0-94e0-dcde583ff35c">IDvdInfo2::GetAudioAttributes</a>
 

 

