---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
ms.date: 07/02/2021
targetos: Windows
description: Represents output arguments to ID3D12VideoEncodeCommandList2::EncodeFrame.
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
req.typenames: D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODEFRAME_OUTPUT_ARGUMENTS
dev_langs:
 - c++
---

## -description

Represents output arguments to [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md).

## -struct-fields

### -field Bitstream

A [A D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM](ns-d3d12video-d3d12_video_encoder_compressed_bitstream.md) containing the result of the encoding operation.

### -field ReconstructedPicture

A [D3D12_VIDEO_ENCODER_RECONSTRUCTED_PICTURE](ns-d3d12video-d3d12_video_encoder_reconstructed_picture.md)  representing a reconstructed picture generated from the input frame. This resource is only needed if the encoded picture is marked to be used as a reference picture in the corresponding picture control structure for this encode operation, NULL can be set otherwise as the reconstructed picture will not be written in the output.

### -field EncoderOutputMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) representing encoding metadata returned by the encoder in hardware-specific layout. This data must be resolved into a readable format using [ID3D12VIDEOCOMMANDLIST2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md).

## -remarks

The caller must check for alignment requirements for the output resources used for the encoding operation.

## -see-also

