---
UID: NE:d3d11_1.D3D11_VIDEO_DECODER_CAPS
title: D3D11_VIDEO_DECODER_CAPS
author: windows-sdk-content
description: Specifies capabilities of the video decoder.
old-location: mf\d3d11_video_decoder_caps.htm
tech.root: medfound
ms.assetid: 8E3C86A4-5F73-4E6F-8F93-5564EA0BC113
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D11_VIDEO_DECODER_CAPS, D3D11_VIDEO_DECODER_CAPS enumeration [Media Foundation], D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE, D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_DYNAMIC, D3D11_VIDEO_DECODER_CAPS_NON_REAL_TIME, d3d11_1/D3D11_VIDEO_DECODER_CAPS, d3d11_1/D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE, d3d11_1/D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_DYNAMIC, d3d11_1/D3D11_VIDEO_DECODER_CAPS_NON_REAL_TIME, mf.d3d11_video_decoder_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_DECODER_CAPS
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_DECODER_CAPS
req.redist: 
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
 

 

