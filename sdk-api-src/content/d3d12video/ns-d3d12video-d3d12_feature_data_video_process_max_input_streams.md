---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
title: D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
description: Retrieves the maximum number of enabled input streams supported by the video processor.
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS","D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS",""]
tech.root: mf
ms.assetid: 7c4f3ea1-e62d-41d2-b277-7e1f08d30dc0
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS, D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS
---

# D3D12_FEATURE_DATA_VIDEO_PROCESS_MAX_INPUT_STREAMS structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_PROCESS\_MAX\_INPUT\_STREAMS](ne-d3d12video-d3d12_feature_video.md). Retrieves the maximum number of enabled input streams supported by the video processor.

## -struct-fields

### -field NodeIndex

An integer indicating which physical adapter of the device the operation applies to, in a multi-adapter operation.

### -field MaxInputStreams

 
The maximum number of streams that can be enabled for the video processor at the same time.

## -remarks

## -see-also

