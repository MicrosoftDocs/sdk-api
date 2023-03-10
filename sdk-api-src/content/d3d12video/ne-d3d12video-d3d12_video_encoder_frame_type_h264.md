---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_FRAME_TYPE_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_TYPE_H264
ms.date: 06/23/2021
targetos: Windows
description: Specifies the type of an H.264 video frame.
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
 - D3D12_VIDEO_ENCODER_FRAME_TYPE_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_TYPE_H264
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_TYPE_H264
dev_langs:
 - c++
---

## -description

Specifies the type of an H.264 video frame.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_H264_I_FRAME

I-Frame. Completely intra-coded frame.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_H264_P_FRAME

P-Frame. Allows references to past frames.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_H264_B_FRAME

B-Frame. Allows references to both past and future (in display order) frames.

### -field D3D12_VIDEO_ENCODER_FRAME_TYPE_H264_IDR_FRAME

Instantaneous decode refresh frame. Special type of I-frame where no frame after it can reference any frame before it.

## -remarks

## -see-also

