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




<a href="https://msdn.microsoft.com/5d60c902-5fb0-419b-b54d-5e3b543c5df8">DMO Enumerated Types</a>



<a href="https://msdn.microsoft.com/9e18bf5e-cf29-4446-a1ba-422b41e02edc">IMediaObject::GetInputStreamInfo</a>
 

 

