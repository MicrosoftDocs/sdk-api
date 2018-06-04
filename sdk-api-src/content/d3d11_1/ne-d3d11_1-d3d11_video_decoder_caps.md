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

# D3D11_VIDEO_DECODER_CAPS enumeration


## -description


Specifies capabilities of the video decoder.


## -enum-fields




### -field D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE

Indicates that the graphics driver supports at least a subset of downsampling operations.


### -field D3D11_VIDEO_DECODER_CAPS_NON_REAL_TIME

Indicates that the decoding hardware cannot support the decode operation in real-time. Decoding is still supported for transcoding scenarios.

With this capability, it is possible that decoding can occur in real-time if downsampling is enabled.



### -field D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_DYNAMIC

Indicates that the driver supports changing down sample parameters after the initial down sample parameters have been applied. For more information, see <a href="https://msdn.microsoft.com/A55D652B-9295-42E4-9A83-CAC467BEE68E">ID3D11VideoContext1::DecoderUpdateDownsampling</a>.


### -field D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_REQUIRED


### -field D3D11_VIDEO_DECODER_CAPS_UNSUPPORTED




## -see-also




<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

