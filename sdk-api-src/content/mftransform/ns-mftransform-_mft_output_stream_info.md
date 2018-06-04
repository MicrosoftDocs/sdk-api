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

# _MFT_OUTPUT_STREAM_INFO structure


## -description



Contains information about an output stream on a Media Foundation transform (MFT). To get these values, call <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">IMFTransform::GetOutputStreamInfo</a>.




## -struct-fields




### -field dwFlags

Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/f67e1e81-baf5-414a-ac23-45d4d6317255">_MFT_OUTPUT_STREAM_INFO_FLAGS</a> enumeration.


### -field cbSize

Minimum size of each output buffer, in bytes. If the MFT does not require a specific size, the value is zero. For uncompressed audio, the value should be the audio frame size, which you can get from the <a href="https://msdn.microsoft.com/7d304826-ad81-4243-a675-2f55b668b348">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> attribute in the media type.

If the <b>dwFlags</b> member contains the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, the value is zero, because the MFT allocates the output buffers.


### -field cbAlignment

The memory alignment required for output buffers. If the MFT does not require a specific alignment, the value is zero. If the <b>dwFlags</b> member contains the MFT_OUTPUT_STREAM_PROVIDES_SAMPLES flag, this value is the alignment that the MFT uses internally when it allocates samples. It is recommended, but not required, that MFTs allocate buffers with at least a 16-byte memory alignment.


## -remarks



Before the media types are set, the only values that should be considered valid is the MFT_OUTPUT_STREAM_OPTIONAL flag in the <b>dwFlags</b> member. This flag indicates that the stream is optional and does not require a media type.

After you set a media type on all of the input and output streams (not including optional streams), all of the values returned by the <a href="https://msdn.microsoft.com/06cc7f1d-57a3-43b8-ab83-8d2ee8e655b5">GetOutputStreamInfo</a> method are valid. They might change if you set different media types.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transforms</a>
 

 

