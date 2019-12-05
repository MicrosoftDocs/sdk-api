---
UID: NE:mediaobj._DMO_INPUT_STREAM_INFO_FLAGS
title: "_DMO_INPUT_STREAM_INFO_FLAGS (mediaobj.h)"
description: The DMO_INPUT_STREAM_INFO_FLAGS enumeration defines flags that describe an input stream.
old-location: dshow\dmo_input_stream_info_flags.htm
tech.root: DirectShow
ms.assetid: 96e37678-0325-4569-8491-c8ef23f6c76e
ms.date: 12/05/2018
ms.keywords: DMO_INPUT_STREAMF_FIXED_SAMPLE_SIZE, DMO_INPUT_STREAMF_HOLDS_BUFFERS, DMO_INPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER, DMO_INPUT_STREAMF_WHOLE_SAMPLES, DMO_INPUT_STREAM_INFO_FLAGS , DMO_INPUT_STREAM_INFO_FLAGSEnumeration, _DMO_INPUT_STREAM_INFO_FLAGS, _DMO_INPUT_STREAM_INFO_FLAGS enumeration [DirectShow], dshow.dmo_input_stream_info_flags, mediaobj/DMO_INPUT_STREAMF_FIXED_SAMPLE_SIZE, mediaobj/DMO_INPUT_STREAMF_HOLDS_BUFFERS, mediaobj/DMO_INPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER, mediaobj/DMO_INPUT_STREAMF_WHOLE_SAMPLES, mediaobj/_DMO_INPUT_STREAM_INFO_FLAGS
ms.topic: enum
f1_keywords: 
 - "mediaobj/_DMO_INPUT_STREAM_INFO_FLAGS"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - _DMO_INPUT_STREAM_INFO_FLAGS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# _DMO_INPUT_STREAM_INFO_FLAGS enumeration


## -description



The <code>DMO_INPUT_STREAM_INFO_FLAGS</code> enumeration defines flags that describe an input stream.




## -enum-fields




### -field DMO_INPUT_STREAMF_WHOLE_SAMPLES

The stream requires whole samples. Samples must not span multiple buffers, and buffers must not contain partial samples.


### -field DMO_INPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER

Each buffer must contain exactly one sample.


### -field DMO_INPUT_STREAMF_FIXED_SAMPLE_SIZE

All the samples in this stream must be the same size.


### -field DMO_INPUT_STREAMF_HOLDS_BUFFERS

The DMO performs lookahead on the incoming data, and may hold multiple input buffers for this stream.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dmo-enumerated-types">DMO Enumerated Types</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo">IMediaObject::GetInputStreamInfo</a>
 

 

