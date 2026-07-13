---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
title: D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
description: Specifies whether a video format and colorspace conversion operation is supported.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_SUPPORT_FLAGS","D3D12_VIDEO_PROCESS_SUPPORT_FLAGS",""]
tech.root: mf
ms.assetid: dc56a715-b29f-42fc-84e9-8ac377b9d0dc
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_SUPPORT_FLAGS, D3D12_VIDEO_PROCESS_SUPPORT_FLAGS,
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
req.typenames: D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_SUPPORT_FLAGS
---

# D3D12_VIDEO_PROCESS_SUPPORT_FLAGS enumeration


## -description

Specifies whether a video format and colorspace conversion operation is supported.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_SUPPORT_FLAG_NONE 

The conversion from the source format and colorspace to destination format and colorspace are not supported.

### -field D3D12_VIDEO_PROCESS_SUPPORT_FLAG_SUPPORTED 

The conversion from the source format and colorspace to destination format and colorspace are supported.

## -remarks

This enumeration is used by the [D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT](ns-d3d12video-d3d12_feature_data_video_process_support.md) structure.

## -see-also

