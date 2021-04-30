---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_FILTER_FLAGS
title: D3D12_VIDEO_PROCESS_FILTER_FLAGS
description: Specifies support for the image filters defined by the D3D12_VIDEO_PROCESS_FILTER enumeration.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_FILTER_FLAGS","D3D12_VIDEO_PROCESS_FILTER_FLAGS"]
tech.root: mf
ms.assetid: 5ed6a952-6333-41d5-ab6e-73332cf2f590
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_FILTER_FLAGS, D3D12_VIDEO_PROCESS_FILTER_FLAGS,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_PROCESS_FILTER_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_FILTER_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_FILTER_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_FILTER_FLAGS
---

# D3D12_VIDEO_PROCESS_FILTER_FLAGS enumeration


## -description

Specifies support for the image filters.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_NONE 

The video processor doesn't support any filters.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_BRIGHTNESS 

The video processor can adjust the brightness level.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_CONTRAST 

The video processor can adjust the contrast level.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_HUE 

The video processor can adjust hue.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_SATURATION 

The video processor can adjust the saturation level.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_NOISE_REDUCTION 

The video processor can perform noise reduction.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_EDGE_ENHANCEMENT 

The video processor can perform edge enhancement.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_ANAMORPHIC_SCALING 

The video processor can perform anamorphic scaling. Anamorphic scaling can be used to stretch 4:3 content to a widescreen 16:9 aspect ratio.

### -field D3D12_VIDEO_PROCESS_FILTER_FLAG_STEREO_ADJUSTMENT 

For stereo 3D video, the video processor can adjust the offset between the left and right views, allowing the user to reduce potential eye strain.

## -remarks

See [D3D12\_VIDEO\_PROCESS\_INPUT\_STREAM\_DESC](ns-d3d12video-d3d12_video_process_input_stream_desc.md) for information on applying a particular filter.

## -see-also

