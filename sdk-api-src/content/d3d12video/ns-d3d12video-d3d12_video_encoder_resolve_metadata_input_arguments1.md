---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
ms.date: 04/07/2026
targetos: Windows
description: Represents input arguments for ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1, with support for optional metadata.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
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
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS1
---

## -description

Represents input arguments for [ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1](nf-d3d12video-id3d12videoencodecommandlist4-resolveencoderoutputmetadata1.md), with support for optional metadata.

## -struct-fields

### -field EncoderCodec

A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the codec of the associated encode operation.

### -field EncoderProfile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the profile for the selected codec in the associated encode operation.

### -field EncoderInputFormat

A [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) specifying the input format of the associated encode operation.

### -field EncodedPictureEffectiveResolution

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) describing the resolution used for the encoding operation.

### -field HWLayoutMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) representing the opaque metadata buffer received from [EncodeFrame1](nf-d3d12video-id3d12videoencodecommandlist4-encodeframe1.md).

### -field OptionalMetadata

A [D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAGS](ne-d3d12video-d3d12_video_encoder_optional_metadata_enable_flags.md) value indicating which optional metadata was enabled during encoding and needs layout resolving.

### -field CodecConfiguration

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_codec_configuration.md) specifying the codec configuration used in the associated **EncodeFrame1** call. Required when any flags are set in *OptionalMetadata*; otherwise pass as zeroed/NULL.

## -remarks

This structure extends [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments.md) with *OptionalMetadata* and *CodecConfiguration* fields.

## -see-also

[ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1](nf-d3d12video-id3d12videoencodecommandlist4-resolveencoderoutputmetadata1.md)

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_input_arguments.md)

