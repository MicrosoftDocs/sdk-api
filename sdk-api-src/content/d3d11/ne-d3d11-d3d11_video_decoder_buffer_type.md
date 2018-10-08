---
UID: NE:d3d11.D3D11_VIDEO_DECODER_BUFFER_TYPE
title: D3D11_VIDEO_DECODER_BUFFER_TYPE
author: windows-sdk-content
description: Specifies a type of compressed buffer for decoding.
old-location: mf\d3d11_video_decoder_buffer_type.htm
tech.root: medfound
ms.assetid: 328B833F-750A-4A88-9571-EAB0532064BD
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: D3D11_VIDEO_DECODER_BUFFER_BITSTREAM, D3D11_VIDEO_DECODER_BUFFER_DEBLOCKING_CONTROL, D3D11_VIDEO_DECODER_BUFFER_FILM_GRAIN, D3D11_VIDEO_DECODER_BUFFER_INVERSE_QUANTIZATION_MATRIX, D3D11_VIDEO_DECODER_BUFFER_MACROBLOCK_CONTROL, D3D11_VIDEO_DECODER_BUFFER_MOTION_VECTOR, D3D11_VIDEO_DECODER_BUFFER_PICTURE_PARAMETERS, D3D11_VIDEO_DECODER_BUFFER_RESIDUAL_DIFFERENCE, D3D11_VIDEO_DECODER_BUFFER_SLICE_CONTROL, D3D11_VIDEO_DECODER_BUFFER_TYPE, D3D11_VIDEO_DECODER_BUFFER_TYPE enumeration [Media Foundation], d3d11/D3D11_VIDEO_DECODER_BUFFER_BITSTREAM, d3d11/D3D11_VIDEO_DECODER_BUFFER_DEBLOCKING_CONTROL, d3d11/D3D11_VIDEO_DECODER_BUFFER_FILM_GRAIN, d3d11/D3D11_VIDEO_DECODER_BUFFER_INVERSE_QUANTIZATION_MATRIX, d3d11/D3D11_VIDEO_DECODER_BUFFER_MACROBLOCK_CONTROL, d3d11/D3D11_VIDEO_DECODER_BUFFER_MOTION_VECTOR, d3d11/D3D11_VIDEO_DECODER_BUFFER_PICTURE_PARAMETERS, d3d11/D3D11_VIDEO_DECODER_BUFFER_RESIDUAL_DIFFERENCE, d3d11/D3D11_VIDEO_DECODER_BUFFER_SLICE_CONTROL, d3d11/D3D11_VIDEO_DECODER_BUFFER_TYPE, mf.d3d11_video_decoder_buffer_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - d3d11.h
api_name:
 - D3D11_VIDEO_DECODER_BUFFER_TYPE
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_BUFFER_TYPE
req.redist: 
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
 

 

