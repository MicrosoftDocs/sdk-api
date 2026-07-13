---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
tech.root: mf
title: D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
ms.date: 06/13/2021
targetos: Windows
description: Represents the GOP structure for multiple video codecs.
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
req.typenames: D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
f1_keywords:
 - D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
 - d3d12video/D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE
dev_langs:
 - c++
---

## -description

Represents the GOP structure for multiple video codecs.

## -struct-fields

### -field DataSize

The data size of the provided encoder GOP structure.

### -field pH264GroupOfPictures

A pointer to a [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_H264](ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_h264.md) representing the GOP structure for H.264 encoding.

### -field pHEVCGroupOfPictures

A pointer to a [D3D12_VIDEO_ENCODER_SEQUENCE_GOP_STRUCTURE_HEVC](ns-d3d12video-d3d12_video_encoder_sequence_gop_structure_hevc.md) representing the GOP structure for H.264 encoding.

## -remarks

## -see-also

