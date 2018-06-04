---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _DMO_OUTPUT_STREAM_INFO_FLAGS enumeration


## -description



The <code>DMO_OUTPUT_STREAM_INFO_FLAGS</code> enumeration defines flags that describe an output stream.




## -enum-fields




### -field DMO_OUTPUT_STREAMF_WHOLE_SAMPLES

The stream contains whole samples. Samples do not span multiple buffers, and buffers do not contain partial samples.


### -field DMO_OUTPUT_STREAMF_SINGLE_SAMPLE_PER_BUFFER

Each buffer contains exactly one sample.


### -field DMO_OUTPUT_STREAMF_FIXED_SAMPLE_SIZE

All the samples in this stream are the same size.


### -field DMO_OUTPUT_STREAMF_DISCARDABLE

The stream is discardable. Within calls to <a href="https://msdn.microsoft.com/1a3b1192-f1e9-4f04-b543-d38692502b8e">IMediaObject::ProcessOutput</a>, the DMO can discard data for this stream without copying it to an output buffer.


### -field DMO_OUTPUT_STREAMF_OPTIONAL

The stream is optional. An optional stream is discardable. Also, the application can ignore this stream entirely; it does not have to set the media type for the stream. Optional streams generally contain additional information, or data not needed by all applications.


## -remarks



The DMO_OUTPUT_STREAMF_DISCARDABLE and DMO_OUTPUT_STREAMF_OPTIONAL flags are mutually exclusive. The DMO can set one of these flags (or neither), but not both.




## -see-also




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/a21e9943-4aaf-4f0e-a92a-5fcd551fe7e1">IMediaObject::GetOutputStreamInfo</a>
 

 

