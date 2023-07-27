---
UID: NE:mediaobj._DMO_OUTPUT_STREAM_INFO_FLAGS
title: "_DMO_OUTPUT_STREAM_INFO_FLAGS (mediaobj.h)"
description: The DMO_OUTPUT_STREAM_INFO_FLAGS enumeration defines flags that describe an output stream.
helpviewer_keywords: ["DMO_OUTPUT_STREAMF_DISCARDABLE","DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE","DMO_OUTPUT_STREAMF_OPTIONAL","DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER","DMO_OUTPUT_STREAMF_WHOLE_SAMPLES","DMO_OUTPUT_STREAM_INFO_FLAGS","DMO_OUTPUT_STREAM_INFO_FLAGSEnumeration","_DMO_OUTPUT_STREAM_INFO_FLAGS","_DMO_OUTPUT_STREAM_INFO_FLAGS enumeration [DirectShow]","dshow.dmo_output_stream_info_flags","mediaobj/DMO_OUTPUT_STREAMF_DISCARDABLE","mediaobj/DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE","mediaobj/DMO_OUTPUT_STREAMF_OPTIONAL","mediaobj/DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER","mediaobj/DMO_OUTPUT_STREAMF_WHOLE_SAMPLES","mediaobj/_DMO_OUTPUT_STREAM_INFO_FLAGS"]
old-location: dshow\dmo_output_stream_info_flags.htm
tech.root: dshow
ms.assetid: 570dd009-0101-4a01-b064-4f4404fb453f
ms.date: 4/26/2023
ms.keywords: DMO_OUTPUT_STREAMF_DISCARDABLE, DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE, DMO_OUTPUT_STREAMF_OPTIONAL, DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER, DMO_OUTPUT_STREAMF_WHOLE_SAMPLES, DMO_OUTPUT_STREAM_INFO_FLAGS , DMO_OUTPUT_STREAM_INFO_FLAGSEnumeration, _DMO_OUTPUT_STREAM_INFO_FLAGS, _DMO_OUTPUT_STREAM_INFO_FLAGS enumeration [DirectShow], dshow.dmo_output_stream_info_flags, mediaobj/DMO_OUTPUT_STREAMF_DISCARDABLE, mediaobj/DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE, mediaobj/DMO_OUTPUT_STREAMF_OPTIONAL, mediaobj/DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER, mediaobj/DMO_OUTPUT_STREAMF_WHOLE_SAMPLES, mediaobj/_DMO_OUTPUT_STREAM_INFO_FLAGS
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
 - _DMO_OUTPUT_STREAM_INFO_FLAGS
 - mediaobj/_DMO_OUTPUT_STREAM_INFO_FLAGS
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
 - _DMO_OUTPUT_STREAM_INFO_FLAGS
---

# _DMO_OUTPUT_STREAM_INFO_FLAGS enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>DMO_OUTPUT_STREAM_INFO_FLAGS</code> enumeration defines flags that describe an output stream.

## -enum-fields

### -field DMO_OUTPUT_STREAMF_WHOLE_SAMPLES:0x1

The stream contains whole samples. Samples do not span multiple buffers, and buffers do not contain partial samples.

### -field DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER:0x2

Each buffer contains exactly one sample.

### -field DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE:0x4

All the samples in this stream are the same size.

### -field DMO_OUTPUT_STREAMF_DISCARDABLE:0x8

The stream is discardable. Within calls to <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a>, the DMO can discard data for this stream without copying it to an output buffer.

### -field DMO_OUTPUT_STREAMF_OPTIONAL:0x10

The stream is optional. An optional stream is discardable. Also, the application can ignore this stream entirely; it does not have to set the media type for the stream. Optional streams generally contain additional information, or data not needed by all applications.

## -remarks

The DMO_OUTPUT_STREAMF_DISCARDABLE and DMO_OUTPUT_STREAMF_OPTIONAL flags are mutually exclusive. The DMO can set one of these flags (or neither), but not both.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo">IMediaObject::GetOutputStreamInfo</a>
