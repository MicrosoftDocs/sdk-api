---
UID: NS:d3d11_4.D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
title: D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
description: Provides data for calls to ID3D11VideoDevice2::CheckFeatureSupport when the feature specified is D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM.
tech.root: direct3d11
helpviewer_keywords: ["D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM"]
ms.date: 4/26/2019
ms.keywords: D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d11_4.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
 - d3d11_4/D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d11_4.h
api_name:
 - D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM
---

## -description

Provides data for calls to [ID3D11VideoDevice2::CheckFeatureSupport](nf-d3d11_4-id3d11videodevice2-checkfeaturesupport.md) when the feature specified is [D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM](ne-d3d11_4-d3d11_feature_video.md). Retrieves the histogram capabilities for the specified decoder configuration.

## -struct-fields

### -field DecoderDesc

A [D3D11_VIDEO_DECODER_DESC](../d3d11/ns-d3d11-d3d11_video_decoder_desc.md) structure containing the decoder description for the decoder to be used with decode histogram.

### -field Components

A bitwise OR combination of values from the [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS](ne-d3d11_4-d3d11_video_decoder_histogram_component_flags.md) enumeration specifying the components of a DXGI_FORMAT for which histogram support will be queried.

### -field BinCount

The number of per component bins supported. This value must be greater than or equal to 64 and must be a power of 2 (e.g. 64, 128, 256, 512...).

### -field CounterBitDepth

The bit depth of the bin counter.  The counter is always stored in a 32-bit value and therefore this value must specify 32 bits or less. The counter is stored in the lower bits of the 32-bit storage.  The upper bits are set to zero.  If the bin count exceeds this bit depth, the value is set to the maximum counter value. Valid values for *CounterBitDepth* are 16, 24, and 32.

## -remarks

## -see-also

[ID3D11VideoDevice2::CheckFeatureSupport](nf-d3d11_4-id3d11videodevice2-checkfeaturesupport.md)
