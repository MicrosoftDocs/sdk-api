---
UID: NS:strmif.tagDVD_MultichannelAudioAttributes
title: DVD_MultichannelAudioAttributes (strmif.h)
description: The DVD_MultichannelAudioAttributes structure describes the multichannel attributes of one audio stream within a specified title.
helpviewer_keywords: ["DVD_MultichannelAudioAttributes","DVD_MultichannelAudioAttributes structure [DirectShow]","DVD_MultichannelAudioAttributesStructure","dshow.dvd_multichannelaudioattributes","strmif/DVD_MultichannelAudioAttributes"]
old-location: dshow\dvd_multichannelaudioattributes.htm
tech.root: dshow
ms.assetid: 8aba7e5a-62ec-4ef5-821f-cfef8cf7d93d
ms.date: 4/26/2023
ms.keywords: DVD_MultichannelAudioAttributes, DVD_MultichannelAudioAttributes structure [DirectShow], DVD_MultichannelAudioAttributesStructure, dshow.dvd_multichannelaudioattributes, strmif/DVD_MultichannelAudioAttributes
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
req.typenames: DVD_MultichannelAudioAttributes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_MultichannelAudioAttributes
 - strmif/tagDVD_MultichannelAudioAttributes
 - DVD_MultichannelAudioAttributes
 - strmif/DVD_MultichannelAudioAttributes
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
 - DVD_MultichannelAudioAttributes
---

# DVD_MultichannelAudioAttributes structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DVD_MultichannelAudioAttributes</code> structure describes the multichannel attributes of one audio stream within a specified title.

## -struct-fields

### -field Info

Array of eight [DVD_MUA_MixingInfo](/windows/desktop/api/strmif/ns-strmif-dvd_mua_mixinginfo) structures, which contain the mixing information for each channel in the audio stream.

### -field Coeff

Array of eight [DVD_MUA_Coeff](/windows/desktop/api/strmif/ns-strmif-dvd_mua_coeff) structures, which contain the mixing coefficients for each channel in the audio stream.

## -remarks

The [DVD_TitleAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_titleattributes) structure contains an array of up to eight <b>DVD_MultichannelAudioAttributes</b> structures. When <code>DVD_TitleAttributes</code> is filled by a call to the <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-gettitleattributes">IDvdInfo2::GetTitleAttributes</a> method, the array will be populated with one <b>DVD_MultichannelAudioAttributes</b> structure for each available audio stream in the title.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>