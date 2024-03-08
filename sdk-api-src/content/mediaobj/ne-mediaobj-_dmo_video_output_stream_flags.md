---
UID: NE:mediaobj._DMO_VIDEO_OUTPUT_STREAM_FLAGS
title: "_DMO_VIDEO_OUTPUT_STREAM_FLAGS (mediaobj.h)"
description: The DMO_VIDEO_OUTPUT_STREAM_FLAGS enumeration defines flags that describe requested features, for video optimizations.
helpviewer_keywords: ["DMO_VIDEO_OUTPUT_STREAM_FLAGS","DMO_VIDEO_OUTPUT_STREAM_FLAGSEnumeration","DMO_VOSF_NEEDS_PREVIOUS_SAMPLE","_DMO_VIDEO_OUTPUT_STREAM_FLAGS","_DMO_VIDEO_OUTPUT_STREAM_FLAGS enumeration [DirectShow]","dshow.dmo_video_output_stream_flags","mediaobj/DMO_VOSF_NEEDS_PREVIOUS_SAMPLE","mediaobj/_DMO_VIDEO_OUTPUT_STREAM_FLAGS"]
old-location: dshow\dmo_video_output_stream_flags.htm
tech.root: dshow
ms.assetid: fafacdd8-d918-491a-a7e5-7b59128f574f
ms.date: 4/26/2023
ms.keywords: DMO_VIDEO_OUTPUT_STREAM_FLAGS , DMO_VIDEO_OUTPUT_STREAM_FLAGSEnumeration, DMO_VOSF_NEEDS_PREVIOUS_SAMPLE, _DMO_VIDEO_OUTPUT_STREAM_FLAGS, _DMO_VIDEO_OUTPUT_STREAM_FLAGS enumeration [DirectShow], dshow.dmo_video_output_stream_flags, mediaobj/DMO_VOSF_NEEDS_PREVIOUS_SAMPLE, mediaobj/_DMO_VIDEO_OUTPUT_STREAM_FLAGS
req.header: mediaobj.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DMO_VIDEO_OUTPUT_STREAM_FLAGS
 - mediaobj/_DMO_VIDEO_OUTPUT_STREAM_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_VIDEO_OUTPUT_STREAM_FLAGS
---

# _DMO_VIDEO_OUTPUT_STREAM_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DMO_VIDEO_OUTPUT_STREAM_FLAGS</code> enumeration defines flags that describe requested features, for video optimizations.

## -enum-fields

### -field DMO_VOSF_NEEDS_PREVIOUS_SAMPLE:0x1

Requests that every output buffer passed to the DMO contain the previous data that was generated.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmovideooutputoptimizations">IDMOVideoOutputOptimizations</a>
