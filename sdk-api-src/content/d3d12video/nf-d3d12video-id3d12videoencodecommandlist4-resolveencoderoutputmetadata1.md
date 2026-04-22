---
UID: NF:d3d12video.ID3D12VideoEncodeCommandList4.ResolveEncoderOutputMetadata1
tech.root: mf
title: ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1
ms.date: 04/07/2026
targetos: Windows
description: Resolves encoder output metadata into a readable format, with support for optional metadata outputs.
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
 - ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1
f1_keywords:
 - ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1
 - d3d12video/ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1
dev_langs:
 - c++
helpviewer_keywords:
 - ResolveEncoderOutputMetadata1
---

## -description

Resolves encoder output metadata into a readable format, with support for optional metadata outputs including QP maps, SATD maps, bit allocation maps, and PSNR data.

## -parameters

### -param pInputArguments

A pointer to a [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments1.md) specifying the input arguments for the resolve operation.

### -param pOutputArguments

A pointer to a [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments1.md) specifying the output arguments for the resolve operation.

## -remarks

This method extends [ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md) by accepting [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments1.md) and [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments1.md), which include optional metadata support.

## -see-also

[ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md)

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments1.md)

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments1.md)

