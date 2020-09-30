---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
title: D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
description: Provides data for calls to ID3D12VideoDevice::CheckFeatureSupport when the feature specified is D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM.
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM","D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM",""]
tech.root: mf
ms.assetid: 052bfdcb-a6f6-4027-811f-9af11b1975b4
ms.date: 11/14/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM, D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_HISTOGRAM](ne-d3d12video-d3d12_feature_video.md). Retrieves the histogram capabilities for the specified decoder configuration.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field DecodeProfile

A GUID representing the decode profile for which histogram capabilities will be queried. Get a list of available profile GUIDs by calling [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_PROFILES](ne-d3d12video-d3d12_feature_video.md).

### -field Width

The decode width of the source stream.

### -field Height

The decode height of the source stream.

### -field DecodeFormat

The [DXGI\_FORMAT](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) representing the decode format.

### -field Components

A bitwise OR combination of values from the [D3D12_VIDEO_DECODE_HISTOGRAM_COMPONENT_FLAGS](ne-d3d12video-d3d12_video_decode_histogram_component_flags.md) enumeration specifying the components of a DXGI_FORMAT for which histogram support will be queried.

### -field BinCount

The number of per component bins supported. This value must be greater than or equal to 64 and must be a power of 2 (e.g. 64, 128, 256, 512...).

### -field CounterBitDepth

 
The bit depth of the bin counter.  The counter is always stored in a 32-bit value and therefore this value must specify 32 bits or less. The counter is stored in the lower bits of the 32-bit storage.  The upper bits are set to zero.  If the bin count exceeds this bit depth, the value is set to the maximum counter value. Valid values for *CounterBitDepth* are 16, 24, and 32.

## -remarks

## -see-also