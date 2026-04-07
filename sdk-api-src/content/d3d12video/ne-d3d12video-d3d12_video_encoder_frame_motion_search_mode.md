---
UID: NE:d3d12video.D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
tech.root: mf
title: D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
ms.date: 04/07/2026
targetos: Windows
description: Specifies motion search modes for video encoding.
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
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
f1_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
 - d3d12video/D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE
---

## -description

Specifies motion search modes for video encoding.

## -enum-fields

### -field D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_FULL_SEARCH : 0

The driver performs the full motion search. When [NumHintsPerPixel](ns-d3d12video-d3d12_video_encoder_input_map_data_motion_vectors.md) is greater than zero, the motion vectors are hints for the driver.

### -field D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT : 1

The driver takes the motion vectors input per pixel, converts them to the codec-specific block partition, and uses the input motion vectors as starting points in the motion search algorithm. The driver is allowed to perform additional motion search to fine-tune and optimize based on the input motion vector hints.

### -field D3D12_VIDEO_ENCODER_FRAME_MOTION_SEARCH_MODE_START_HINT_LIMITED_DISTANCE : 2

The driver takes the motion vectors input per pixel, converts them to the codec-specific block partition, and uses the input motion vectors as starting points in the motion search algorithm. The driver is allowed to perform limited motion search to fine-tune and optimize, but the resulting new motion vectors must not deviate more than [SearchDeviationLimit](ns-d3d12video-d3d12_video_encoder_frame_motion_search_mode_config.md) percent in terms of Euclidean vector distance from the input motion vector.

## -remarks

## -see-also
