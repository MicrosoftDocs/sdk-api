---
UID: NE:d3d11_4.D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
title: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
description: Specifies indices for arrays of per component histogram information.
tech.root: direct3d11
helpviewer_keywords: ["D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT"]
ms.date: 4/26/2019
ms.keywords: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d11_4.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
 - d3d11_4/D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d11_4.h
api_name:
 - D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
---

## -description

Specifies indices for arrays of per component histogram information.

## -enum-fields

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_Y:0

If the format is a YUV format, indicates a histogram for the Y component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_U:1

If the format is a YUV format, indicates a histogram for the U component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_V:2

If the format is a YUV format, indicates a histogram for the V component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_R:0

If the format is an RGB/BGR format, indicates a histogram for the R component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_G:1

If the format is an RGB/BGR format, indicates a histogram for the G component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_B:2

If the format is an RGB/BGR format, indicates a histogram for the B component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_A:3

If the format has an alpha channel, indicates a histogram for the A component.

## -remarks

The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS](ne-d3d11_4-d3d11_video_decoder_histogram_component_flags.md) is the flags enumeration used by [D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM](ns-d3d11_4-d3d11_feature_data_video_decoder_histogram.md) to allow you to specify one or more components for which histogram data is queried.

## -see-also

