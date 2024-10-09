---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList2.ResolveEncoderOutputMetadata
tech.root: mf
title: ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata
ms.date: 07/02/2021
targetos: Windows
description: Resolves the output metadata from a call to ID3D12VideoEncodeCommandList2::EncodeFrame to a readable format.
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
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
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
 - ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata
f1_keywords:
 - ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata
 - d3d12video/ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata
dev_langs:
 - c++
---

## -description

Resolves the output metadata from a call to [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) to a readable format.

## -parameters

### -param pInputArguments

A pointer to a [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments.md), containing a pointer to the opaque [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](ns-d3d12video-d3d12_video_encoder_output_metadata.md) received from a previous call to **EncodeFrame**.

### -param pOutputArguments

A pointer to a [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments.md), containing a pointer to the [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](ns-d3d12video-d3d12_video_encoder_output_metadata.md) where the resolved, readable metadata will be written.

## -remarks

The caller can interpret the contents of *pOutputArguments* as a memory blob that contains a [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](ns-d3d12video-d3d12_video_encoder_output_metadata.md) structure and the metadata array contents. The array contents of the dynamic size metadata based on the subregion number are positioned in memory contiguously right after the struct allocation and the pointers in the struct point to the start addresses of the array contents.

## -see-also

