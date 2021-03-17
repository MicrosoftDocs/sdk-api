---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
title: D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
description: Retrieves the number of past and future reference frames required for the specified deinterlace mode, filter, rate conversion, or auto processing features.
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO","D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO",""]
tech.root: mf
ms.assetid: 4d1ee0ed-59a3-4a6d-b636-9fb0bd3e5141
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO, D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO,
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO
---

# D3D12_FEATURE_DATA_VIDEO_PROCESS_REFERENCE_INFO structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_PROCESS\_REFERENCE\_INFO](ne-d3d12video-d3d12_feature_video.md). Retrieves the number of past and future reference frames required for the specified deinterlace mode, filter, rate conversion, or auto processing features.

## -struct-fields

### -field NodeIndex

An integer indicating which physical adapter of the device the operation applies to, in a multi-adapter operation.

### -field DeinterlaceMode

A member of the [D3D12\_VIDEO\_PROCESS\_DEINTERLACE\_FLAGS](ne-d3d12video-d3d12_video_process_deinterlace_flags.md) enumeration specifying the deinterlacing mode for which the required past and future reference frame counts are retrieved.

### -field Filters

A bitwise OR combination of values from the [D3D12\_VIDEO\_PROCESS\_FILTER\_FLAGS](ne-d3d12video-d3d12_video_process_filter_flags.md) enumeration specifying the filters for which the required past and future reference frame counts are retrieved.

### -field FeatureSupport

A bitwise OR combination of values from the [D3D12\_VIDEO\_PROCESS\_FEATURE\_FLAGS](ne-d3d12video-d3d12_video_process_feature_flags.md) enumeration specifying the features for which the required past and future reference frame counts are retrieved.

### -field InputFrameRate

The input frame rate of the stream for which the required past and future reference frame counts are retrieved.

### -field OutputFrameRate

The output frame rate of the stream for which the required past and future reference frame counts are retrieved.

### -field EnableAutoProcessing

True if autoprocessing will be used; otherwise, false.

### -field PastFrames

The number of past frames required to support the specified processing features.

### -field FutureFrames

 
The number of future frames required to support the specified processing features.

## -remarks

## -see-also

