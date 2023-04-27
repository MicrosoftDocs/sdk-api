---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
title: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
description: Flags for indicating a subset of components used with video decode histogram. (D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS)
helpviewer_keywords: ["D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS","D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS",""]
tech.root: mf
ms.assetid: d2806ba5-882b-4f69-9867-b271002681ba
ms.date: 11/14/2019
ms.keywords: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS, D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS,
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
req.typenames: D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
 - d3d12video/D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS
---

# D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS enumeration


## -description

Flags for indicating a subset of components used with video decode histogram. This enumeration is used by the [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](ns-d3d12video-d3d12_feature_data_video_decode_histogram.md) structure.

## -enum-fields

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_NONE 

No associated component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_Y 

If the format is a YUV format, indicates the Y component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_U 

If the format is a YUV format, indicates the U component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_V 

If the format is a YUV format, indicates the V component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_R 

If the format is an RGB/BGR format, indicates the R component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_G 

If the format is an RGB/BGR format, indicates the G component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_B 

If the format is an RGB/BGR format, indicates the B component.

### -field D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAG_A 

If the format is an RGB/BGR format, indicates the A component.

## -remarks

## -see-also

