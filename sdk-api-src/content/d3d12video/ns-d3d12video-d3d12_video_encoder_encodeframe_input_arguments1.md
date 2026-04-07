---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
tech.root: mf
title: D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
ms.date: 04/07/2026
targetos: Windows
description: Represents input arguments for ID3D12VideoEncodeCommandList4::EncodeFrame1, with support for optional metadata.
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
req.typenames: D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
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
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
f1_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS1
---

## -description

Represents input arguments for [ID3D12VideoEncodeCommandList4::EncodeFrame1](nf-d3d12video-id3d12videoencodecommandlist4-encodeframe1.md), with support for optional metadata.

## -struct-fields

### -field SequenceControlDesc

A [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md) specifying the configuration for the video encoding sequence.

### -field PictureControlDesc

A [D3D12_VIDEO_ENCODER_PICTURE_CONTROL_DESC](ns-d3d12video-d3d12_video_encoder_picture_control_desc.md) specifying the configuration for the video encoding picture.

### -field pInputFrame

A pointer to the [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) representing the input frame to encode.

### -field InputFrameSubresource

The subresource index of the input frame.

### -field CurrentFrameBitstreamMetadataSize

The expected size in bytes of the current frame bitstream metadata.

### -field OptionalMetadata

A [D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAGS](ne-d3d12video-d3d12_video_encoder_optional_metadata_enable_flags.md) value indicating which optional metadata to enable when encoding this frame.

## -remarks

This structure extends [D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments.md) with the *OptionalMetadata* field.

## -see-also

[ID3D12VideoEncodeCommandList4::EncodeFrame1](nf-d3d12video-id3d12videoencodecommandlist4-encodeframe1.md)

[D3D12_VIDEO_ENCODER_ENCODEFRAME_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_encodeframe_input_arguments.md)

