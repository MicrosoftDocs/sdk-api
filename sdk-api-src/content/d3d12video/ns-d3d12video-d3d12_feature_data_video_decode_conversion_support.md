---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT
title: D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT
description: Retrieves the list of supported profiles.
tech.root: mf
ms.assetid: 916f29f6-8bb5-4ac8-94a4-5cea6bdf353b
ms.date: 05/28/2019
ms.topic: struct
f1_keywords:
- D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT
dev_langs:
- c++
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT, D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT,
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- d3d12video.h
api_name:
- D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT
targetos: Windows
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_CONVERSION_SUPPORT structure

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_CONVERSION\_SUPPORT](ne-d3d12video-d3d12_feature_video). Retrieves the list of supported profiles. Check if a colorspace conversion, format conversion, and scale are supported.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, identifies the physical adapter of the device this operation applies to.
 
### -field Configuration

A [D3D12\_VIDEO\_DECODE\_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration) structure describing the decode configuration.

### -field DecodeSample

A [D3D12\_VIDEO\_SAMPLE](ns-d3d12video-d3d12_video_sample) structure representing the source decoded as sample description.  
 
### -field OutputFormat

A [D3D12\_VIDEO\_FORMAT](ns-d3d12video-d3d12_video_format) structure containing the output sample description.

### -field FrameRate

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time.
 
### -field BitRate

The average bits per second data compression rate for the compressed video stream.  This is used by the driver to determine whether the video can be decoded in real-time.
 
### -field SupportFlags

A combination of values from the [D3D12\_VIDEO\_DECODE\_CONVERSION\_SUPPORT\_FLAGS](ne-d3d12video-d3d12_video_decode_conversion_support_flags) indicating the support for the specified conversion.
 
### -field ScaleSupport
 
A [D3D12\_VIDEO\_SCALE\_SUPPORT](ns-d3d12video-d3d12_video_scale_support) structure representing the output size range for decode conversion.

## -remarks

If the colorspace and format conversion is supported, *ScaleFlags* will have the [D3D12\_VIDEO\_SCALE\_SUPPORT\_FLAGS](ne-d3d12video-d3d12_video_scale_support_flags) set. Callers should check the [D3D12\_VIDEO\_SIZE\_RANGE](ns-d3d12video-d3d12_video_size_range) field to determine if the requested scale is supported.

## -see-also

[D3D12_FEATURE_VIDEO_DECODE_CONVERSION_SUPPORT](ne-d3d12video-d3d12_feature_video)
