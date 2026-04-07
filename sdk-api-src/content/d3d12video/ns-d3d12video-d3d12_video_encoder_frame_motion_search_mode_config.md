---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
ms.date: 04/07/2026
targetos: Windows
description: Specifies the motion search mode configuration.
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
req.target-min-winverclnt:
req.target-min-winversvr:
req.target-type:
req.typenames: D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
req.umdf-ver:
req.unicode-ansi:
typedef_isUnnamed: false
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_CONFIG
---

## -description

Specifies the motion search mode and associated parameters for how the driver uses motion vector hints.

## -struct-fields

### -field MotionSearchMode

A [D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE](ne-d3d12video-d3d12_video_encoder_frame_motion_search_mode.md) specifying the mode in which the driver uses motion vector hints.

### -field SearchDeviationLimit

The maximum allowed percent deviation in Euclidean vector distance from the input motion vector. Used with D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE.

## -remarks

## -see-also
