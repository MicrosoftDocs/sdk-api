---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
title: D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
description: Retrieves support information for video decoding.
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT","D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT",""]
tech.root: mf
ms.assetid: 2a7019a1-e3a8-49ca-b094-12e1f45b43e3
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT, D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT,
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_SUPPORT](ne-d3d12video-d3d12_feature_video.md). Retrieves support information for video decoding.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Configuration

A [D3D12\_VIDEO\_DECODE\_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration.md) structure specifying the decode profile, bitstream encryption, and interlace type of the source stream.

### -field Width

The decode width of the source stream.

### -field Height

The decode height of the source stream

### -field DecodeFormat

The [DXGI\_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) to use as the decode format.  This format is the output format if no decoder conversion is specified.

### -field FrameRate

The frame rate of the video format. A value of 0 means the frame rate is unknown.

### -field BitRate

The average bits per second data compression rate for the compressed video stream.  This information is used by the driver to determine whether the video can be decoded in real-time. A value of 0 means the bit rate is unknown.

### -field SupportFlags

 
A combination of values from the [D3D12\_VIDEO\_DECODE\_SUPPORT\_FLAGS](ne-d3d12video-d3d12_video_decode_support_flags.md) enumeration indicating the support for video decoding. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.

### -field ConfigurationFlags

A combination of values from the [D3D12\_VIDEO\_DECODE\_CONFIGURATION\_FLAGS](ne-d3d12video-d3d12_video_decode_configuration_flags.md) enumeration describing the video decode configuration. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.

### -field DecodeTier

A member of the [D3D12\_VIDEO\_DECODE\_TIER](ne-d3d12video-d3d12_video_decode_tier.md) enumeration specifying the decoding tier of a hardware video decoder.

## -remarks

## -see-also