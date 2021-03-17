---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
title: D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
description: Specifies the automatic processing features that a video processor can support.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS","D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS",""]
tech.root: mf
ms.assetid: 4a93c0be-32e7-4c7a-a015-3195490280cb
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS, D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS,
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
req.typenames: D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS
---

# D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS enumeration


## -description

Specifies the automatic processing features that a video processor can support.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_NONE 

No automatic processing features are supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_DENOISE 

Denoise is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_DERINGING 

Deringing is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_EDGE_ENHANCEMENT 

Edge enhancement is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_COLOR_CORRECTION 

Color correction is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_FLESH_TONE_MAPPING 

Flesh tone mapping is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_IMAGE_STABILIZATION 

Image stabilization is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_SUPER_RESOLUTION 

Enhanced image resolution is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_ANAMORPHIC_SCALING 

Anamorphic scaling is supported.

### -field D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAG_CUSTOM 

Additional processing features, not described by the other flags, are available.

## -remarks

This enumeration is used by the [D3D12\_FEATURE\_DATA\_VIDEO\_PROCESS\_SUPPORT](ns-d3d12video-d3d12_feature_data_video_process_support.md) structure.

## -see-also

