---
UID: NE:mediaobj._DMO_OUTPUT_STREAM_INFO_FLAGS
title: "_DMO_OUTPUT_STREAM_INFO_FLAGS (mediaobj.h)"
description: The DMO_OUTPUT_STREAM_INFO_FLAGS enumeration defines flags that describe an output stream.
helpviewer_keywords: ["DMO_OUTPUT_STREAMF_DISCARDABLE","DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE","DMO_OUTPUT_STREAMF_OPTIONAL","DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER","DMO_OUTPUT_STREAMF_WHOLE_SAMPLES","DMO_OUTPUT_STREAM_INFO_FLAGS","DMO_OUTPUT_STREAM_INFO_FLAGSEnumeration","_DMO_OUTPUT_STREAM_INFO_FLAGS","_DMO_OUTPUT_STREAM_INFO_FLAGS enumeration [DirectShow]","dshow.dmo_output_stream_info_flags","mediaobj/DMO_OUTPUT_STREAMF_DISCARDABLE","mediaobj/DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE","mediaobj/DMO_OUTPUT_STREAMF_OPTIONAL","mediaobj/DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER","mediaobj/DMO_OUTPUT_STREAMF_WHOLE_SAMPLES","mediaobj/_DMO_OUTPUT_STREAM_INFO_FLAGS"]
old-location: dshow\dmo_output_stream_info_flags.htm
tech.root: dshow
ms.assetid: 570dd009-0101-4a01-b064-4f4404fb453f
ms.date: 12/05/2018
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
