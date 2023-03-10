---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
ms.date: 07/02/2021
targetos: Windows
description: Represents output arguments for a call to ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS
dev_langs:
 - c++
---

## -description

Represents output arguments for a call to [ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md).

## -struct-fields

### -field ResolvedLayoutMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) representing the resolved metadata buffer.

This buffer must be read back to the CPU by the caller and cast to a [D3D12_VIDEO_ENCODER_OUTPUT_METADATA](ns-d3d12video-d3d12_video_encoder_output_metadata.md) structure. The remaining data in the buffer, corresponds to **D3D12_VIDEO_ENCODER_OUTPUT_METADATA.WrittenSubregionsCount** packed entries of type [D3D12_VIDEO_ENCODER_FRAME_SUBREGION_METADATA](ns-d3d12video-d3d12_video_encoder_frame_subregion_metadata.md).

## -remarks

The following diagram illustrates the resolved metadata memory layout in an ID3D12Resource.

:::image type="content" source="images/d3d12-video-resolved-metadata-layout.png" alt-text="Diagram of the resolved metadata memory layout in an ID3D12Resource":::

## -see-also

