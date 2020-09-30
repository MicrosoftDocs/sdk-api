---
UID: NE:d3d12video.D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
title: D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
description: Specifies flags for video processing input streams.
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS","D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS",""]
tech.root: mf
ms.assetid: d27ae6b9-c5e2-4f46-a76c-2f91bb8b9ba7
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS, D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
 - d3d12video/D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS
---

# D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAGS enumeration


## -description

Specifies flags for video processing input streams. Used by the [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](ns-d3d12video-d3d12_video_process_input_stream_arguments.md) structure.

## -enum-fields

### -field D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAG_NONE 

No flags specified.

### -field D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAG_FRAME_DISCONTINUITY 

Set this flag when not processing frames in order, such as seeking between frames

### -field D3D12_VIDEO_PROCESS_INPUT_STREAM_FLAG_FRAME_REPEAT 

Set this flag when applying video process operation to the same set of inputs.

## -remarks

## -see-also

