---
UID: NE:d3d11_4.D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS
title: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS
description: Flags for indicating a subset of components used with video decode histogram.
ms.date: 4/26/2019
ms.keywords: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS
ms.topic: language-reference
f1_keywords:
- D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS
dev_langs:
- c++
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d11_4.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- d3d11_4.h
api_name:
- D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS
---

## -description

Flags for indicating a subset of components used with video decode histogram. This enumeration is used by the [D3D12_FEATURE_DATA_VIDEO_DECODE_HISTOGRAM](ns-d3d12video-d3d12_feature_data_video_decode_histogram) structure.

## -enum-fields

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_NONE

No associated component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_Y

If the format is a YUV format, indicates the Y component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_U

If the format is a YUV format, indicates the U component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_V

If the format is a YUV format, indicates the V component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_R

If the format is an RGB/BGR format, indicates the R component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_G

If the format is an RGB/BGR format, indicates the G component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_B

If the format is an RGB/BGR format, indicates the B component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAG_A

If the format is an RGB/BGR format, indicates the A component.

## -remarks

## -see-also

