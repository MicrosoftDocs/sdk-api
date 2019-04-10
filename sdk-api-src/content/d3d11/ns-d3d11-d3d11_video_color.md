---
UID: NS:d3d11.D3D11_VIDEO_COLOR
title: D3D11_VIDEO_COLOR (d3d11.h)
author: windows-sdk-content
description: Defines a color value for Microsoft Direct3D 11 video.
old-location: mf\d3d11_video_color.htm
tech.root: medfound
ms.assetid: F8E070EE-F8F6-4AAF-9A8A-6D0AF6B857B5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_COLOR, D3D11_VIDEO_COLOR structure [Media Foundation], d3d11/D3D11_VIDEO_COLOR, mf.d3d11_video_color
ms.topic: struct
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
 - D3D11_VIDEO_COLOR
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_COLOR
req.redist: 
---

# D3D11_VIDEO_COLOR structure


## -description


Defines a color value for Microsoft Direct3D 11 video.


## -struct-fields




### -field YCbCr

A <a href="https://msdn.microsoft.com/242D6032-62E5-4915-B074-6E595A12F912">D3D11_VIDEO_COLOR_YCbCrA</a> structure that contains a YCbCr color value.




### -field RGBA

A <a href="https://msdn.microsoft.com/DDD587DC-BB17-407D-9E9E-47015950A504">D3D11_VIDEO_COLOR_RGBA</a> structure that contains an RGB color value.




## -remarks



The anonymous union can represent both RGB and YCbCr colors. The interpretation of the union depends on the context.






## -see-also




<a href="https://msdn.microsoft.com/089f42f2-1e5b-4d4b-98a4-9ef0ca2823c1">About YUV Video</a>



<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

