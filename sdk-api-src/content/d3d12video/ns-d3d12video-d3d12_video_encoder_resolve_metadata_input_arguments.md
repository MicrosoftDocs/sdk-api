---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
ms.date: 07/02/2021
targetos: Windows
description: Represents input arguments for a call to ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_METADATA_INPUT_ARGUMENTS
dev_langs:
 - c++
---

## -description

Represents input arguments for a call to [ID3D12VideoEncodeCommandList2::ResolveEncoderOutputMetadata](nf-d3d12video-id3d12videoencodecommandlist2-resolveencoderoutputmetadata.md).

## -struct-fields

### -field EncoderCodec

A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the codec of the associated encode operation.

### -field EncoderProfile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the profile for the selected codec in the associated encode operation.

### -field EncoderInputFormat

A [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) specifying the input format of the associated encode operation.

### -field EncodedPictureEffectiveResolution

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) structure describing the resolution used for the encoding operation.

### -field HWLayoutMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) representing the associated opaque metadata buffer received from [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md).

## -remarks

## -see-also

