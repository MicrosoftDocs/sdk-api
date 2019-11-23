---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT
title: D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT

description: Provides data for calls to ID3D12VideoDevice::CheckFeatureSupport when the feature specified is D3D12_FEATURE_VIDEO_PROCESS_SUPPORT.
tech.root: mf
ms.assetid: 29911ed2-9509-4fbd-8e18-c7b5a9e2d397

ms.date: 05/28/2019 
ms.topic: struct
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT
dev_langs:
 - c++
ms.keywords: D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT, D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT, 
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT
topic_type: 
 - apiref
api_type: 
 - HeaderDef
api_location: 
 - d3d12video.h
api_name: 
 - D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT
targetos: Windows
---

# D3D12_FEATURE_DATA_VIDEO_PROCESS_SUPPORT structure

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is [D3D12\_FEATURE\_VIDEO\_PROCESS\_SUPPORT ](ne-d3d12video-d3d12_feature_video).


## -struct-fields

### -field NodeIndex

An integer indicating which physical adapter of the device the operation applies to, in a multi-adapter operation. 

### -field InputSample

A [D3D12\_VIDEO\_SAMPLE](ns-d3d12video-d3d12_video_sample) structure defining the width, height, and format of the input sample.
 
### -field InputFieldType

A member of the [D3D12\_VIDEO\_FIELD\_TYPE](ne-d3d12video-d3d12_video_field_type) enumeration specifying the interlaced field type of the input sample. 
 
### -field InputStereoFormat

A member of the [D3D12\_VIDEO\_FRAME\_STEREO\_FORMAT](ne-d3d12video-d3d12_video_frame_stereo_format) enumeration specifying the stereo format of the input sample. 
 
### -field InputFrameRate

The input frame rate.
 
### -field OutputFormat

A [D3D12\_VIDEO\_FORMAT](ns-d3d12video-d3d12_video_format) structure specifying the output DXGI format and color space.
 
### -field OutputStereoFormat

A member of the [D3D12\_VIDEO\_FRAME\_STEREO\_FORMAT](ne-d3d12video-d3d12_video_frame_stereo_format) enumeration specifying the stereo format of the output. 
 
### -field OutputFrameRate

The output frame rate.
 
### -field SupportFlags

A member of the [D3D12\_VIDEO\_PROCESS\_SUPPORT\_FLAGS](ne-d3d12video-d3d12_video_process_support_flags) indicating whether the requested format and colorspace conversion is supported. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.

 
### -field ScaleSupport

A [D3D12\_VIDEO\_SCALE\_SUPPORT](ns-d3d12video-d3d12_video_scale_support) structure specifying the supported scaling capabilities. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field FeatureSupport

A bitwise OR combination of values from the [D3D12\_VIDEO\_PROCESS\_FEATURE\_FLAGS](ne-d3d12video-d3d12_video_process_feature_flags) enumeration specifying the supported video processing features. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field DeinterlaceSupport

A member of the [D3D12\_VIDEO\_PROCESS\_DEINTERLACE\_FLAGS](ne-d3d12video-d3d12_video_process_deinterlace_flags) enumeration specifying the supported deinterlacing capabilities. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field AutoProcessingSupport

A member of the [D3D12\_VIDEO\_PROCESS\_AUTO\_PROCESSING\_FLAGS](ne-d3d12video-d3d12_video_process_auto_processing_flags) specifying the supported automatic processing capabilities. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field FilterSupport

A bitwise OR combination of values from the [D3D12\_VIDEO\_PROCESS\_FILTER\_FLAGS](ne-d3d12video-d3d12_video_process_filter_flags) enumeration specifying the supported video filtering features. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field FilterRangeSupport
 
An array of [D3D12\_VIDEO\_PROCESS\_FILTER\_RANGE](ns-d3d12video-d3d12_video_process_filter_range) structures representing the filter range values.  This value is populated by the call to **ID3D12Device::CheckFeatureSupport**. The calling application must allocate the memory for the filter range list before calling **CheckFeatureSupport**.

## -remarks

## -see-also
