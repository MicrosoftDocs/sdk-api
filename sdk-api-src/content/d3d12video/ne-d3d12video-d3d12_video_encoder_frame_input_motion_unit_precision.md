---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
ms.date: 04/07/2026
targetos: Windows
description: Specifies the numerical unit precision for input motion vectors.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d12video.h
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
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION
---

## -description

Defines the numerical unit used in input motion vector and rect values. For example, D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_FULL_PIXEL indicates that a vector (-2, 3) represents a -2 pixel shift in X and a 3 pixel shift in Y. For D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_HALF_PIXEL, the same vector represents a -1 pixel shift in X and a 1.5 pixel shift in Y.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_FULL_PIXEL : 0

Full pixel precision.

### -field D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_HALF_PIXEL : 1

Half pixel precision.

### -field D3D12_VIDEO_ENCODER_FRAME_INPUT_MOTION_UNIT_PRECISION_QUARTER_PIXEL : 2

Quarter pixel precision.

## -remarks

## -see-also
