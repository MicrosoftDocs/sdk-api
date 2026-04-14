---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
ms.date: 04/07/2026
targetos: Windows
description: Describes input arguments for the ResolveInputParamLayout operation.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
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
 - D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS
---

## -description

Describes input arguments for [ID3D12VideoEncodeCommandList4::ResolveInputParamLayout](nf-d3d12video-id3d12videoencodecommandlist4-resolveinputparamlayout.md).

## -struct-fields

### -field SessionInfo

A [D3D12_VIDEO_ENCODER_INPUT_MAP_SESSION_INFO](ns-d3d12video-d3d12_video_encoder_input_map_session_info.md) containing information pertaining to the encoding session.

### -field InputData

A [D3D12_VIDEO_ENCODER_INPUT_MAP_DATA](ns-d3d12video-d3d12_video_encoder_input_map_data.md) containing the input data along with the input type being resolved.

## -remarks

## -see-also
