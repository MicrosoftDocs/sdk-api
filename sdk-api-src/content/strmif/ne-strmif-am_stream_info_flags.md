---
UID: NE:strmif.AM_STREAM_INFO_FLAGS
title: AM_STREAM_INFO_FLAGS (strmif.h)
description: The AM_STREAM_INFO_FLAGS enumeration defines flags that indicate a pin's stream-control status.
helpviewer_keywords: ["AM_STREAM_INFO_DISCARDING","AM_STREAM_INFO_FLAGS","AM_STREAM_INFO_FLAGS","AM_STREAM_INFO_FLAGS enumeration [DirectShow]","AM_STREAM_INFO_FLAGSEnumeration","AM_STREAM_INFO_START_DEFINED","AM_STREAM_INFO_STOP_DEFINED","AM_STREAM_INFO_STOP_SEND_EXTRA","dshow.am_stream_info_flags","strmif/AM_STREAM_INFO_DISCARDING","strmif/AM_STREAM_INFO_FLAGS","strmif/AM_STREAM_INFO_START_DEFINED","strmif/AM_STREAM_INFO_STOP_DEFINED","strmif/AM_STREAM_INFO_STOP_SEND_EXTRA"]
old-location: dshow\am_stream_info_flags.htm
tech.root: dshow
ms.assetid: 48f6ab36-f019-4096-b6e7-6f6ebc7c454a
ms.date: 4/26/2023
ms.keywords: AM_STREAM_INFO_DISCARDING, AM_STREAM_INFO_FLAGS, AM_STREAM_INFO_FLAGS , AM_STREAM_INFO_FLAGS enumeration [DirectShow], AM_STREAM_INFO_FLAGSEnumeration, AM_STREAM_INFO_START_DEFINED, AM_STREAM_INFO_STOP_DEFINED, AM_STREAM_INFO_STOP_SEND_EXTRA, dshow.am_stream_info_flags, strmif/AM_STREAM_INFO_DISCARDING, strmif/AM_STREAM_INFO_FLAGS, strmif/AM_STREAM_INFO_START_DEFINED, strmif/AM_STREAM_INFO_STOP_DEFINED, strmif/AM_STREAM_INFO_STOP_SEND_EXTRA
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
req.typenames: AM_STREAM_INFO_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AM_STREAM_INFO_FLAGS
 - strmif/AM_STREAM_INFO_FLAGS
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
 - AM_STREAM_INFO_FLAGS
---

# AM_STREAM_INFO_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_STREAM_INFO_FLAGS</b> enumeration defines flags that indicate a pin's stream-control status.

## -enum-fields

### -field AM_STREAM_INFO_START_DEFINED:0x1

Indicates that the pin's start time is set.

### -field AM_STREAM_INFO_STOP_DEFINED:0x2

Indicates that the pin's stop time is been set.

### -field AM_STREAM_INFO_DISCARDING:0x4

Indicates that the pin is currently discarding data.

### -field AM_STREAM_INFO_STOP_SEND_EXTRA:0x10

Indicates that the pin will send one extra sample after it reaches the stop time.

## -see-also

<a href="/windows/desktop/api/strmif/ns-strmif-am_stream_info">AM_STREAM_INFO</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamstreamcontrol-getinfo">IAMStreamControl::GetInfo</a>
