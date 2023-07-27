---
UID: NE:strmif._DECIMATION_USAGE
title: DECIMATION_USAGE (strmif.h)
description: Describes the strategy that the Overlay Mixer Filter filter uses to scale the video image down to a smaller size.
helpviewer_keywords: ["DECIMATION_DEFAULT","DECIMATION_LEGACY","DECIMATION_USAGE","DECIMATION_USAGE","DECIMATION_USAGE enumeration [DirectShow]","DECIMATION_USAGEEnumeration","DECIMATION_USE_DECODER_ONLY","DECIMATION_USE_OVERLAY_ONLY","DECIMATION_USE_VIDEOPORT_ONLY","dshow.decimation_usage","strmif/DECIMATION_DEFAULT","strmif/DECIMATION_LEGACY","strmif/DECIMATION_USAGE","strmif/DECIMATION_USE_DECODER_ONLY","strmif/DECIMATION_USE_OVERLAY_ONLY","strmif/DECIMATION_USE_VIDEOPORT_ONLY"]
old-location: dshow\decimation_usage.htm
tech.root: dshow
ms.assetid: 4c39f7f9-2d9c-4db5-9a2b-cf221ddedf80
ms.date: 4/26/2023
ms.keywords: DECIMATION_DEFAULT, DECIMATION_LEGACY, DECIMATION_USAGE, DECIMATION_USAGE , DECIMATION_USAGE enumeration [DirectShow], DECIMATION_USAGEEnumeration, DECIMATION_USE_DECODER_ONLY, DECIMATION_USE_OVERLAY_ONLY, DECIMATION_USE_VIDEOPORT_ONLY, dshow.decimation_usage, strmif/DECIMATION_DEFAULT, strmif/DECIMATION_LEGACY, strmif/DECIMATION_USAGE, strmif/DECIMATION_USE_DECODER_ONLY, strmif/DECIMATION_USE_OVERLAY_ONLY, strmif/DECIMATION_USE_VIDEOPORT_ONLY
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
req.typenames: DECIMATION_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DECIMATION_USAGE
 - strmif/_DECIMATION_USAGE
 - DECIMATION_USAGE
 - strmif/DECIMATION_USAGE
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
 - DECIMATION_USAGE
---

# DECIMATION_USAGE enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Describes the strategy that the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> filter uses to scale the video image down to a smaller size.

## -enum-fields

### -field DECIMATION_LEGACY:0

Decimate the video by taking the following steps, in the order listed, until one of them succeeds.

<ol>
<li>Try to use the overlay scaler on the VGA chip.</li>
<li>If the Overlay Mixer is connected through a video port, try to use the scaler on the video port.</li>
<li>Crop the video image.</li>
</ol>

### -field DECIMATION_USE_DECODER_ONLY

Decimate using the scaler on the video decoder. If that fails, crop the video image.

### -field DECIMATION_USE_VIDEOPORT_ONLY

Decimate using the scaler on the video port. If that fails, crop the video image.

### -field DECIMATION_USE_OVERLAY_ONLY

Decimate using the overlay scaler on the VGA chip. If that fails, crop the video image.

### -field DECIMATION_DEFAULT

Decimate the video by taking the following steps, in the order listed, until one of them succeeds.

<ol>
<li>Try to use the scaler on the video decoder.</li>
<li>Try to use the overlay scaler on the VGA chip.</li>
<li>If the Overlay Mixer is connected through a video port, try to use the scaler on the video port.</li>
<li>Crop the video image.</li>
</ol>
This mode is the default decimation strategy.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamvideodecimationproperties">IAMVideoDecimationProperties</a>
