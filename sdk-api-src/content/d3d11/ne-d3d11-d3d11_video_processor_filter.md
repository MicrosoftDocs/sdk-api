---
UID: NE:d3d11.D3D11_VIDEO_PROCESSOR_FILTER
title: D3D11_VIDEO_PROCESSOR_FILTER (d3d11.h)
description: Identifies a video processor filter.
helpviewer_keywords: ["D3D11_VIDEO_PROCESSOR_FILTER","D3D11_VIDEO_PROCESSOR_FILTER enumeration [Media Foundation]","D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING","D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS","D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST","D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT","D3D11_VIDEO_PROCESSOR_FILTER_HUE","D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION","D3D11_VIDEO_PROCESSOR_FILTER_SATURATION","D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT","d3d11/D3D11_VIDEO_PROCESSOR_FILTER","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_HUE","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_SATURATION","d3d11/D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT","mf.d3d11_video_processor_filter"]
old-location: mf\d3d11_video_processor_filter.htm
tech.root: mf
ms.assetid: 87CF9A1A-E196-4B5A-BAAE-DD948A5468C2
ms.date: 12/05/2018
ms.keywords: D3D11_VIDEO_PROCESSOR_FILTER, D3D11_VIDEO_PROCESSOR_FILTER enumeration [Media Foundation], D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING, D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS, D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST, D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT, D3D11_VIDEO_PROCESSOR_FILTER_HUE, D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION, D3D11_VIDEO_PROCESSOR_FILTER_SATURATION, D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_HUE, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_SATURATION, d3d11/D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT, mf.d3d11_video_processor_filter
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
targetos: Windows
req.typenames: D3D11_VIDEO_PROCESSOR_FILTER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VIDEO_PROCESSOR_FILTER
 - d3d11/D3D11_VIDEO_PROCESSOR_FILTER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_VIDEO_PROCESSOR_FILTER
---

# D3D11_VIDEO_PROCESSOR_FILTER enumeration


## -description

Identifies a video processor filter.

## -enum-fields

### -field D3D11_VIDEO_PROCESSOR_FILTER_BRIGHTNESS:0

Brightness filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_CONTRAST:1

Contrast filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_HUE:2

Hue filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_SATURATION:3

Saturation filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_NOISE_REDUCTION:4

Noise reduction filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_EDGE_ENHANCEMENT:5

Edge enhancement filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_ANAMORPHIC_SCALING:6

Anamorphic scaling filter.

### -field D3D11_VIDEO_PROCESSOR_FILTER_STEREO_ADJUSTMENT:7

Stereo adjustment filter. When stereo 3D video is enabled, this filter adjusts the offset between the left and right views, allowing the user to reduce potential eye strain. 

The filter value indicates the amount by which the left and right views are adjusted.  A positive value shifts the images away from each other: the left image toward the left, and the right image toward the right. A negative value shifts the images in the opposite directions, closer to each other.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorsetstreamfilter">ID3D11VideoContext::VideoProcessorSetStreamFilter</a>
