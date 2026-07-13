---
UID: NE:d3d11_1.D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
title: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS (d3d11_1.h)
description: Specifies flags that indicate the most efficient methods for performing video processing operations.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS","D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION","D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE","D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION","D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT","d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS","d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION","d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE","d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION","d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT","mf.d3d11_video_processor_behavior_hints"]
old-location: mf\d3d11_video_processor_behavior_hints.htm
tech.root: mf
ms.assetid: 0EB7F918-EA7A-4E7E-9B6D-53F582CC6B28
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION, D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION, d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT, mf.d3d11_video_processor_behavior_hints
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
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
 - d3d11_1/D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_1.h
api_name:
 - D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
---

# D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS enumeration


## -description

Specifies flags that indicate the most efficient methods for performing video processing operations.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_ROTATION:0x1

Multi-plane overlay hardware can perform the rotation operation more efficiently than the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_RESIZE:0x2

Multi-plane overlay hardware can perform the scaling operation more efficiently than the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_MULTIPLANE_OVERLAY_COLOR_SPACE_CONVERSION:0x4

Multi-plane overlay hardware can perform the colorspace conversion operation more efficiently than the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> method.

### -field D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINT_TRIPLE_BUFFER_OUTPUT:0x8

The video processor output data should be at least triple buffered for optimal performance.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>
