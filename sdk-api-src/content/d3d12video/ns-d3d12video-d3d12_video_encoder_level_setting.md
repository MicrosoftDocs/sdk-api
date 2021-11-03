---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_LEVEL_SETTING
tech.root: mf
title: D3D12_VIDEO_ENCODER_LEVEL_SETTING
ms.date: 06/04/2021
targetos: Windows
description: Represents a video encoder level setting.
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
req.typenames: D3D12_VIDEO_ENCODER_LEVEL_SETTING
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_LEVEL_SETTING
f1_keywords:
 - D3D12_VIDEO_ENCODER_LEVEL_SETTING
 - d3d12video/D3D12_VIDEO_ENCODER_LEVEL_SETTING
dev_langs:
 - c++
---

## -description

Represents a video encoder level setting.

## -struct-fields

### -field DataSize

The data size of the provided encoder level setting.

### -field pH264LevelSetting

A pointer to a value from the [D3D12_VIDEO_ENCODER_LEVELS_H264](ne-d3d12video-d3d12_video_encoder_levels_h264.md) enumeration specifying an H.264 level.

### -field pHEVCLevelSetting

A pointer to a  [D3D12_VIDEO_ENCODER_LEVEL_TIER_CONSTRAINTS_HEVC](ns-d3d12video-d3d12_video_encoder_level_tier_constraints_hevc.md) structure specifying an HEVC profile.

## -remarks

## -see-also

