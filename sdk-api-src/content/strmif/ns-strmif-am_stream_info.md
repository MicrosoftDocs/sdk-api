---
UID: NS:strmif.AM_STREAM_INFO
title: AM_STREAM_INFO (strmif.h)
description: The AM_STREAM_INFO structure contains stream-control information.
helpviewer_keywords: ["AM_STREAM_INFO","AM_STREAM_INFO structure [DirectShow]","AM_STREAM_INFOStructure","dshow.am_stream_info","strmif/AM_STREAM_INFO"]
old-location: dshow\am_stream_info.htm
tech.root: dshow
ms.assetid: 63b62f03-1973-41af-b6a4-e1bcb6ab803f
ms.date: 4/26/2023
ms.keywords: AM_STREAM_INFO, AM_STREAM_INFO structure [DirectShow], AM_STREAM_INFOStructure, dshow.am_stream_info, strmif/AM_STREAM_INFO
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
req.typenames: AM_STREAM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_STREAM_INFO
 - strmif/AM_STREAM_INFO
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
 - AM_STREAM_INFO
---

# AM_STREAM_INFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The AM_STREAM_INFO structure contains stream-control information.

## -struct-fields

### -field tStart

Time when the pin will start streaming data.

### -field tStop

Time when the pin will stop streaming data.

### -field dwStartCookie

Value that will be sent with the event notification when the pin starts.

### -field dwStopCookie

Value that will be sent with the event notification when the pin stops.

### -field dwFlags

Bitwise combination of zero or more flags from the <a href="/windows/desktop/api/strmif/ne-strmif-am_stream_info_flags">AM_STREAM_INFO_FLAGS</a> enumeration.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-getinfo">IAMStreamControl::GetInfo</a>