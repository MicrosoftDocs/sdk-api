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

# D3D11_VIDEO_DECODER_BUFFER_TYPE enumeration


## -description


Specifies a type of compressed buffer for decoding.


## -enum-fields




### -field D3D11_VIDEO_DECODER_BUFFER_PICTURE_PARAMETERS

Picture decoding parameter buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_MACROBLOCK_CONTROL

Macroblock control command buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_RESIDUAL_DIFFERENCE

Residual difference block data buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_DEBLOCKING_CONTROL

Deblocking filter control command buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_INVERSE_QUANTIZATION_MATRIX

Inverse quantization matrix buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_SLICE_CONTROL

Slice-control buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_BITSTREAM

Bitstream data buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_MOTION_VECTOR

Motion vector buffer.



### -field D3D11_VIDEO_DECODER_BUFFER_FILM_GRAIN

Film grain synthesis data buffer.



## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>



<a href="https://msdn.microsoft.com/6842D5D7-6165-4428-91BD-2234BE5332B8">ID3D11VideoContext::GetDecoderBuffer</a>
 

 

