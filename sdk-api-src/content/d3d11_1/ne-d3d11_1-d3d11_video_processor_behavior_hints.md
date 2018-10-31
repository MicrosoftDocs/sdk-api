---
UID: NE:d3d11_1.D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
title: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
author: windows-sdk-content
description: Specifies flags that indicate the most efficient methods for performing video processing operations.
old-location: mf\d3d11_video_processor_behavior_hints.htm
tech.root: medfound
ms.assetid: 0EB7F918-EA7A-4E7E-9B6D-53F582CC6B28
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT, mf.d3d11_video_processor_behavior_hints
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
 - D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
product: Windows
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
req.redist: 
---

# D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS enumeration


## -description


Specifies flags that indicate the most efficient methods for performing video processing operations. 


## -enum-fields




### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION

Multi-plane overlay hardware can perform the rotation operation more efficiently than the <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> method.


### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE

Multi-plane overlay hardware can perform the scaling operation more efficiently than the <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> method.


### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION

Multi-plane overlay hardware can perform the colorspace conversion operation more efficiently than the <a href="https://msdn.microsoft.com/en-us/library/Hh447719(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorBlt</a> method.


### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT

The video processor output data should be at least triple buffered for optimal performance.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447678(v=VS.85).aspx">Direct3D 11 Video Enumerations</a>
 

 

