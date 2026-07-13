---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList4.ResolveInputParamLayout
tech.root: mf
title: ID3D12VideoEncodeCommandList4::ResolveInputParamLayout
ms.date: 04/07/2026
targetos: Windows
description: Converts input map layouts into hardware-specific opaque layouts.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d12video.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12video.h
api_name:
 - ID3D12VideoEncodeCommandList4::ResolveInputParamLayout
f1_keywords:
 - ID3D12VideoEncodeCommandList4::ResolveInputParamLayout
 - d3d12video/ID3D12VideoEncodeCommandList4::ResolveInputParamLayout
dev_langs:
 - c++
---

## -description

Converts from the hardware-agnostic input layouts of the maps defined in this API into the hardware-specific opaque layouts.

## -parameters

### -param pInputArguments

A [D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_input_param_layout_input_arguments.md) specifying the input data to resolve.

### -param pOutputArguments

A [D3D12_VIDEO_ENCODER_RESOLVE_INPUT_PARAM_LAYOUT_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_input_param_layout_output_arguments.md) specifying the output buffer for the resolved opaque layout.

## -remarks

Input resources must be in **D3D12_RESOURCE_STATE_VIDEO_ENCODE_READ** and output resources in **D3D12_RESOURCE_STATE_VIDEO_ENCODE_WRITE** before executing this command.

## -see-also
