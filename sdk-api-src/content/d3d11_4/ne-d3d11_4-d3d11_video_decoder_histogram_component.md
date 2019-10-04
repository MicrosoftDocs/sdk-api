---
UID: NE:d3d11_4.D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
title: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
description: Specifies indices for arrays of per component histogram infromation.
ms.date: 4/26/2019
ms.keywords: D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
ms.topic: language-reference
f1_keywords:
 - D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
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
 - D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT
---

## -description

Specifies indices for arrays of per component histogram infromation.

## -enum-fields

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_Y

If the format is a YUV format, indicates a histogram for the Y component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_U

If the format is a YUV format, indicates a histogram for the U component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_V

If the format is a YUV format, indicates a histogram for the V component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_R

If the format is an RGB/BGR format, indicates a histogram for the R component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_G

If the format is an RGB/BGR format, indicates a histogram for the G component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_B

If the format is an RGB/BGR format, indicates a histogram for the B component.

### -field D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_A

If the format has an alpha channel, indicates a histogram for the A component.

## -remarks

The [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT_FLAGS](ne-d3d11_4-d3d11_video_decoder_histogram_component_flags) is the flags enumeration used by [D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM](ns-d3d11_4-d3d11_feature_data_video_decoder_histogram) to allow you to specify one or more components for which histogram data is queried.

## -see-also

