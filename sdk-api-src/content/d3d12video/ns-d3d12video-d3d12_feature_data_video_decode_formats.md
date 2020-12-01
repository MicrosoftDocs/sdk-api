---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
title: D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
description: Retrieves the list of supported formats.
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS","D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS",""]
tech.root: mf
ms.assetid: 685f27d9-b54d-40ca-a156-3bd85b8cae74
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS, D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS,
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_FORMATS structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_FORMAT](ne-d3d12video-d3d12_feature_video.md). Retrieves the list of supported formats.

## -struct-fields

### -field NodeIndex

 
For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field Configuration

A [D3D12\_VIDEO\_DECODE\_CONFIGURATION](ns-d3d12video-d3d12_video_decode_configuration.md) structure describing the decode configuration for the list of formats.

### -field FormatCount

The number of formats to retrieve.  This number must match the value returned from a call [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_FORMAT\_COUNT](ne-d3d12video-d3d12_feature_video.md).

### -field pOutputFormats

A list of [DXGI_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) structures representing the supported formats.

## -remarks

## -see-also