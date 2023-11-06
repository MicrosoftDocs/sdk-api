---
UID: NE:strmif._AM_DVD_STREAM_FLAGS
title: AM_DVD_STREAM_FLAGS (strmif.h)
description: Describes a DVD stream type (video, audio, or subpicture).
helpviewer_keywords: ["AM_DVD_STREAM_AUDIO","AM_DVD_STREAM_FLAGS","AM_DVD_STREAM_FLAGS","AM_DVD_STREAM_FLAGS enumeration [DirectShow]","AM_DVD_STREAM_FLAGSEnumeration","AM_DVD_STREAM_SUBPIC","AM_DVD_STREAM_VIDEO","dshow.am_dvd_stream_flags","strmif/AM_DVD_STREAM_AUDIO","strmif/AM_DVD_STREAM_FLAGS","strmif/AM_DVD_STREAM_SUBPIC","strmif/AM_DVD_STREAM_VIDEO"]
old-location: dshow\am_dvd_stream_flags.htm
tech.root: dshow
ms.assetid: 3fb3e57f-7c0b-4a49-b83d-798c84b2d5d1
ms.date: 4/26/2023
ms.keywords: AM_DVD_STREAM_AUDIO, AM_DVD_STREAM_FLAGS, AM_DVD_STREAM_FLAGS , AM_DVD_STREAM_FLAGS enumeration [DirectShow], AM_DVD_STREAM_FLAGSEnumeration, AM_DVD_STREAM_SUBPIC, AM_DVD_STREAM_VIDEO, dshow.am_dvd_stream_flags, strmif/AM_DVD_STREAM_AUDIO, strmif/AM_DVD_STREAM_FLAGS, strmif/AM_DVD_STREAM_SUBPIC, strmif/AM_DVD_STREAM_VIDEO
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
req.typenames: AM_DVD_STREAM_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AM_DVD_STREAM_FLAGS
 - strmif/_AM_DVD_STREAM_FLAGS
 - AM_DVD_STREAM_FLAGS
 - strmif/AM_DVD_STREAM_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - AM_DVD_STREAM_FLAGS
---

# AM_DVD_STREAM_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Describes a DVD stream type (video, audio, or subpicture).

## -enum-fields

### -field AM_DVD_STREAM_VIDEO:0x1

DVD video stream.

### -field AM_DVD_STREAM_AUDIO:0x2

DVD audio stream.

### -field AM_DVD_STREAM_SUBPIC:0x4

DVD subpicture stream.

## -see-also

[AM_DVD_RENDERSTATUS Structure](/windows/desktop/api/strmif/ns-strmif-am_dvd_renderstatus)



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
