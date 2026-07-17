---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
ms.date: 04/07/2026
targetos: Windows
description: Represents output arguments for ID3D12VideoEncodeCommandList4::EncodeFrame1, with support for subregion notification.
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
req.typenames: D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS1
---

## -description

Represents output arguments for [ID3D12VideoEncodeCommandList4::EncodeFrame1](nf-d3d12video-id3d12videoencodecommandlist4-encodeframe1.md), with support for subregion notification.

## -struct-fields

### -field Bitstream

A [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM1](ns-d3d12video-d3d12_video_encoder_compressed_bitstream1.md) containing the result of the encoding operation.

### -field ReconstructedPicture

A [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE](ns-d3d12video-d3d12_video_encoder_reconstructed_picture.md) representing a reconstructed picture generated from the input frame. This resource is only needed if the encoded picture is marked to be used as a reference picture in the corresponding picture control structure. Set to NULL otherwise.

### -field EncoderOutputMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) representing encoding metadata returned by the encoder in hardware-specific layout. This data must be resolved into a readable format using [ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md).

### -field FrameAnalysisReconstructedPicture

A [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE](ns-d3d12video-d3d12_video_encoder_reconstructed_picture.md) for the frame analysis reconstructed picture, used with the frame analysis (two-pass encoding) feature.

## -remarks

The caller must check for alignment requirements for the output resources used in the encoding operation.

## -see-also

[ID3D12VideoEncodeCommandList4::EncodeFrame1](nf-d3d12video-id3d12videoencodecommandlist4-encodeframe1.md)

[D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_encodeframe_output_arguments.md)

