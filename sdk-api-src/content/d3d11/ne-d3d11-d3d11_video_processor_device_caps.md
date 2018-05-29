---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_DEVICE_CAPS
title: D3D11_VIDEO_PROCESSOR_DEVICE_CAPS
author: windows-sdk-content
description: Defines video processing capabilities for a Microsoft Direct3D 11 video processor.
old-location: mf\d3d11_video_processor_device_caps.htm
old-project: medfound
ms.assetid: 35335C16-D8BD-4C52-9C9A-4B28DCB53A7F
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_DEVICE_CAPS, D3D11_VIDEO_PROCESSOR_DEVICE_CAPS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_LINEAR_SPACE, D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_NOMINAL_RANGE, D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_RGB_RANGE_CONVERSION, D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_xvYCC, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_LINEAR_SPACE, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_NOMINAL_RANGE, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_RGB_RANGE_CONVERSION, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION, d3d11/D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_xvYCC, mf.d3d11_video_processor_device_caps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VIDEO_PROCESSOR_DEVICE_CAPS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11.h
api_name:
-	D3D11_VIDEO_PROCESSOR_DEVICE_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_VIDEO_PROCESSOR_DEVICE_CAPS enumeration


## -description


Defines video processing capabilities for a Microsoft Direct3D 11 video processor.


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_LINEAR_SPACE

The video processor can blend video content in linear color space. Most video content is gamma corrected, resulting in nonlinear values. This capability flag means that the video processor converts colors to linear space before blending, which produces better results.


### -field D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_xvYCC

The video processor supports the xvYCC color space for YCbCr data.




### -field D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_RGB_RANGE_CONVERSION

The video processor can perform range conversion when the input and output are both RGB but use different color ranges (0-255 or 16-235, for 8-bit RGB).




### -field D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_YCbCr_MATRIX_CONVERSION

The video processor can apply a matrix conversion to YCbCr values when the input and output are both YCbCr. For example, the driver can convert colors from BT.601 to BT.709.




### -field D3D11_VIDEO_PROCESSOR_DEVICE_CAPS_NOMINAL_RANGE

The video processor supports YUV nominal range . 

Supported in Windows 8.1 and later.


## -see-also




<a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a>



<a href="https://msdn.microsoft.com/40061AD1-BCD9-4170-A442-34B4C792BB55">Direct3D 11 Video Enumerations</a>
 

 

