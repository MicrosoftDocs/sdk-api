---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
title: D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
description: Specifies the deinterlacing video processor capabilities.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS","D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS",""]
tech.root: mf
ms.assetid: 7f25af81-344c-4a70-9d58-9eed1604c11a
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS, D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS,
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
req.typenames: D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS
---

# D3D12_VIDEO_PROCESS_DEINTERLACE_FLAGS enumeration


## -description

Specifies the deinterlacing video processor capabilities.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_DEINTERLACE_FLAG_NONE 

No deinterlacing capabilities are available.

### -field D3D12_VIDEO_PROCESS_DEINTERLACE_FLAG_BOB 

The video processor can perform bob deinterlacing. In bob deinterlacing, missing field lines are interpolated from the lines above and below. Bob deinterlacing does not require reference frames.

### -field D3D12_VIDEO_PROCESS_DEINTERLACE_FLAG_CUSTOM 

The video processor can perform a custom high-quality deinterlacing, which requires the number of reference frames indicated in *PastFrames* and *FutureFrames* output fields of the <a href="ns-d3d12video-d3d12_feature_data_video_process_reference_info.md">D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO</a> populated by a call to <a href="nf-d3d12video-id3d12videodevice-checkfeaturesupport.md">ID3D12VideoDevice::CheckFeatureSupport</a> when the feature specified is <a href="ne-d3d12video-d3d12_feature_video.md">D3D12_FEATURE_VIDEO_PROCESS_REFERENCE_INFO</a>. If the video processor doesn’t have the necessary number of reference frames, it falls back to bob deinterlacing.

## -remarks

## -see-also

