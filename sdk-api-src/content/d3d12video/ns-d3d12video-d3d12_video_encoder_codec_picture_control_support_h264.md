---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
tech.root: mf
title: D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
ms.date: 06/09/2021
targetos: Windows
description: Represents picture control support settings for H.264 video encoding.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
f1_keywords:
 - D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
 - d3d12video/D3D12_VIDEO_ENCODER_CODEC_PICTURE_CONTROL_SUPPORT_H264
dev_langs:
 - c++
---

## -description

Represents picture control support settings for H.264 video encoding.

## -struct-fields

### -field MaxL0ReferencesForP

The maximum value allowed in the slice headers for (num_ref_idx_l0_active_minus1 +1) when encoding P frames. This is equivalent to the maximum size of an L0 for a P frame supported.

### -field MaxL0ReferencesForB

The maximum value allowed in the slice headers for (num_ref_idx_l0_active_minus1 +1) when encoding B frames. This is equivalent to the maximum size of an L0 for a B frame supported.

### -field MaxL1ReferencesForB

The maximum value allowed in the slice headers for (num_ref_idx_l1_active_minus1 +1) when encoding B frames. This is equivalent to the maximum size of an L1 for a B frame supported.

### -field MaxLongTermReferences

The maximum number of references used in a frame that can be marked as long term reference.

### -field MaxDPBCapacity

The maximum number of unique pictures that can be used from the DPB the caller manages (number of unique indices in L0 union L1) for a given [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) command on the underlying hardware.

## -remarks

## -see-also

