---
UID: NS:dvdmedia.tagAM_DvdKaraokeData
title: AM_DvdKaraokeData (dvdmedia.h)
description: Specifies how to mix the karaoke audio channels.
helpviewer_keywords: ["AM_DvdKaraokeData","AM_DvdKaraokeData structure [DirectShow]","dshow.am_dvdkaraokedata","dvdmedia/AM_DvdKaraokeData"]
old-location: dshow\am_dvdkaraokedata.htm
tech.root: dshow
ms.assetid: 9fef2dd9-0a56-4e51-a64b-7f12c8f9a966
ms.date: 4/26/2023
ms.keywords: AM_DvdKaraokeData, AM_DvdKaraokeData structure [DirectShow], dshow.am_dvdkaraokedata, dvdmedia/AM_DvdKaraokeData
req.header: dvdmedia.h
req.include-header: 
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
req.typenames: AM_DvdKaraokeData
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAM_DvdKaraokeData
 - dvdmedia/tagAM_DvdKaraokeData
 - AM_DvdKaraokeData
 - dvdmedia/AM_DvdKaraokeData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dvdmedia.h
api_name:
 - AM_DvdKaraokeData
---

# AM_DvdKaraokeData structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Specifies how to mix the karaoke audio channels.

## -struct-fields

### -field dwDownmix

A bitwise OR of <a href="/windows/win32/api/strmif/ne-strmif-dvd_karaoke_downmix">DVD_KARAOKE_DOWNMIX</a> flags telling the decoder which channels are downmixed to channels 0 or 1.

### -field dwSpeakerAssignment

A valid <a href="/windows/win32/api/strmif/ne-strmif-dvd_karaoke_assignment">DVD_KARAOKE_ASSIGNMENT</a> value that indicates which speakers the output is going to.

## -remarks

This structure is used for the AM_PROPERTY_DVDKARAOKE_DATA property.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-karaoke-property-set">DVD Karaoke Property Set</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode">SelectKaraokeAudioPresentationMode</a>