---
UID: NS:strmif.tagDVD_AudioAttributes
title: DVD_AudioAttributes (strmif.h)
description: The DVD_AudioAttributes structure is used in IDvdInfo2::GetAudioAttributes to receive the various audio attributes of the disc.helpviewer_keywords: ["DVD_AudioAttributes","DVD_AudioAttributes structure [DirectShow]","DVD_AudioAttributesStructure","dshow.dvd_audioattributes","strmif/DVD_AudioAttributes"]
old-location: dshow\dvd_audioattributes.htm
tech.root: DirectShow
ms.assetid: a4365c05-718e-4d48-bb2c-a13a609df82f
ms.date: 12/05/2018
ms.keywords: DVD_AudioAttributes, DVD_AudioAttributes structure [DirectShow], DVD_AudioAttributesStructure, dshow.dvd_audioattributes, strmif/DVD_AudioAttributes
f1_keywords:
- strmif/DVD_AudioAttributes
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
- DVD_AudioAttributes
targetos: Windows
req.typenames: DVD_AudioAttributes
req.redist: 
ms.custom: 19H1
---

# DVD_AudioAttributes structure


## -description



The <code>DVD_AudioAttributes</code> structure is used in <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getaudioattributes">IDvdInfo2::GetAudioAttributes</a> to receive the various audio attributes of the disc.




## -struct-fields




### -field AppMode

Indicates the current audio mode. If the mode returned is DVD_AudioMode_Karaoke, call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getkaraokeattributes">IDvdInfo2::GetKaraokeAttributes</a> to get more info.


### -field AppModeData

 


### -field AudioFormat

Describes the format (encoding mode) of the audio stream.


### -field Language

An <b>LCID</b> value indicating the language of the audio stream. Is zero if no language is present.


### -field LanguageExtension

A [DVD_AUDIO_LANG_EXT](https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_audio_lang_ext) enumeration that will be filled in if any information is available on the disc.


### -field fHasMultichannelInfo

Indicates whether multichannel attributes are present. If <b>TRUE</b>, it means there is additional mixing information available, such as for SurroundSound. Call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a> to retrieve the multichannel information.


### -field dwFrequency

The frequency in hertz (48k, 96k) of the audio stream.


### -field bQuantization

The resolution of the audio stream (16, 20, 24 bits, or other) Zero indicates the resolution is unknown.


### -field bNumberOfChannels

The number of channels. For example, 5.1 Dolby AC-3 has six channels.


### -field dwReserved

Reserved.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

