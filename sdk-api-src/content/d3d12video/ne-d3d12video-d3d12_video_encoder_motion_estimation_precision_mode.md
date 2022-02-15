---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE
ms.date: 06/10/2021
targetos: Windows
description: Specifies motion estimation precision modes for video encoding.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE
dev_langs:
 - c++
---

## -description

Specifies motion estimation precision modes for video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE_MAXIMUM

No limit in the precision for motion estimation vectors. This mode allows the maximum precision supported by the driver.

### -field D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE_FULL_PIXEL

The precision for motion estimation vectors has to be at most full pixel.

### -field D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE_HALF_PIXEL

The precision for motion estimation vectors has to be at most half pixel.

### -field D3D12_VIDEO_ENCODER_MOTION_ESTIMATION_PRECISION_MODE_QUARTER_PIXEL

The precision for motion estimation vectors has to be at most quarter pixel.

## -remarks

## -see-also

