---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
title: D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
description: Retrieves support information for video decoding.
tech.root: mf
ms.assetid: 2a7019a1-e3a8-49ca-b094-12e1f45b43e3
ms.date: 05/28/2019
ms.topic: struct
f1_keywords:
- D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
dev_langs:
- c++
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
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- d3d12video.h
api_name:
- D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT
targetos: Windows
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT structure

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_SUPPORT](ne-d3d12video-d3d12_feature_video). Retrieves support information for video decoding.

## -struct-fields

### -field NodeIndex

An integer indicating which physical adapter of the device the operation applies to, in a multi-adapter operation. 
 
### -field Configuration

A [D3D12\_VIDEO\_DECODE\_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration) structure specifying the decode profile, bitstream encryption, and interlace type of the source stream.
 
### -field Width

The decode width of the source stream.
 
### -field Height

The decode height of the source stream
 
### -field DecodeFormat

The [DXGI\_FORMAT](https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) to use as the decode format.  This format is the output format if no decoder conversion is specified.
 
### -field FrameRate

The frame rate of the video format. A value of 0 means the frame rate is unknown.
 
### -field BitRate

The average bits per second data compression rate for the compressed video stream.  This information is used by the driver to determine whether the video can be decoded in real-time. A value of 0 means the bit rate is unknown.
 
### -field SupportFlags
 
A combination of values from the [D3D12\_VIDEO\_DECODE\_SUPPORT\_FLAGS](ne-d3d12video-d3d12_video_decode_support_flags) enumeration indicating the support for video decoding. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.

### -field ConfigurationFlags

A combination of values from the [D3D12\_VIDEO\_DECODE\_CONFIGURATION\_FLAGS](ne-d3d12video-d3d12_video_decode_configuration_flags) eumeration describing the video decode configuration. This value is populated by the call to **ID3D12Device::CheckFeatureSupport**.
 
### -field DecodeTier

A member of the [D3D12\_VIDEO\_DECODE\_TIER](ne-d3d12video-d3d12_video_decode_tier) enumeration specifying the decoding tier of a hardware video decoder.
 

## -remarks

## -see-also
