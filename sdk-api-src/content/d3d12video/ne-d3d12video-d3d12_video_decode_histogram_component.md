---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
title: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
description: Specifies indices for arrays of per component histogram information. (D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT","D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT",""]
tech.root: mf
ms.assetid: e503a4a5-9a6d-4c2d-8f6e-1fe0e2e24c22
ms.date: 11/14/2019
ms.keywords: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT, D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT,
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
req.typenames: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
 - d3d12video/D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT
---

# D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT enumeration


## -description

Specifies indices for arrays of per component histogram information.

## -enum-fields

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_Y 

If the format is a YUV format, indicates a histogram for the Y component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_U 

If the format is a YUV format, indicates a histogram for the U component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_V 

If the format is a YUV format, indicates a histogram for the V component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_R 

If the format is an RGB/BGR format, indicates a histogram for the R component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_G 

If the format is an RGB/BGR format, indicates a histogram for the G component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_B 

If the format is an RGB/BGR format, indicates a histogram for the B component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_A 

If the format has an alpha channel, indicates a histogram for the A component.

## -remarks

The [D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS](ne-d3d12video-d3d12_video_decode_histogram_component_flags.md) is the flags enumeration used by [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](ns-d3d12video-d3d12_feature_data_video_decode_histogram.md) to allow you to specify one or more components for which histogram data is queried.

## -see-also

