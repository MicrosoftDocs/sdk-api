---
UID: NS:strmif.__MIDL___MIDL_itf_strmif_0000_0138_0001
title: AM_DVD_RENDERSTATUS (strmif.h)
description: The AM_DVD_RENDERSTATUS structure contains codes indicating the status of DVD-Video playback. These codes are used in the IDvdGraphBuilder::RenderDvdVideoVolume method.
helpviewer_keywords: ["AM_DVD_RENDERSTATUS","AM_DVD_RENDERSTATUS structure [DirectShow]","AM_DVD_RENDERSTATUSStructure","dshow.am_dvd_renderstatus","strmif/AM_DVD_RENDERSTATUS"]
old-location: dshow\am_dvd_renderstatus.htm
tech.root: dshow
ms.assetid: 6d11332e-86db-4649-af77-2906c6cbba7a
ms.date: 4/26/2023
ms.keywords: AM_DVD_RENDERSTATUS, AM_DVD_RENDERSTATUS structure [DirectShow], AM_DVD_RENDERSTATUSStructure, dshow.am_dvd_renderstatus, strmif/AM_DVD_RENDERSTATUS
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
req.typenames: AM_DVD_RENDERSTATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_strmif_0000_0138_0001
 - strmif/__MIDL___MIDL_itf_strmif_0000_0138_0001
 - AM_DVD_RENDERSTATUS
 - strmif/AM_DVD_RENDERSTATUS
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
 - AM_DVD_RENDERSTATUS
---

# AM_DVD_RENDERSTATUS structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The AM_DVD_RENDERSTATUS structure contains codes indicating the status of DVD-Video playback. These codes are used in the <a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a> method.

## -struct-fields

### -field hrVPEStatus

Overlay/VPE error code. Zero indicates success; any other value is failure.

### -field bDvdVolInvalid

<b>TRUE</b> if the specified DVD volume to be played does not exist; <b>FALSE</b> otherwise.

### -field bDvdVolUnknown

<b>TRUE</b> if no DVD volume is specified or if it isn't found; <b>FALSE</b> otherwise.

### -field bNoLine21In

<b>TRUE</b> if the video decoder doesn't produce line 21 (closed captioning) data; <b>FALSE</b> otherwise.

### -field bNoLine21Out

<b>TRUE</b> if the video decoder can't be shown as closed captioning on video due to a problem with graph building; <b>FALSE</b> otherwise.

### -field iNumStreams

Number of DVD streams to render.

### -field iNumStreamsFailed

Number of streams that failed to render.

### -field dwFailedStreamsFlag

Combination of [AM_DVD_STREAM_FLAGS](/windows/win32/api/strmif/ne-strmif-am_dvd_stream_flags) flags indicating which streams failed.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-idvdgraphbuilder-renderdvdvideovolume">IDvdGraphBuilder::RenderDvdVideoVolume</a>