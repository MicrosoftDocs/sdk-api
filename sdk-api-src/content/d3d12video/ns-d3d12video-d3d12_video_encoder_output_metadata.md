---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_OUTPUT_METADATA
tech.root: mf
title: D3D12_VIDEO_ENCODER_OUTPUT_METADATA
ms.date: 07/02/2021
targetos: Windows
description: Represents metadata about an ID3D12VideoEncodeCommandList2::EncodeFrame operation.
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
req.typenames: D3D12_VIDEO_ENCODER_OUTPUT_METADATA
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_ENCODER_OUTPUT_METADATA
f1_keywords:
 - D3D12_VIDEO_ENCODER_OUTPUT_METADATA
 - d3d12video/D3D12_VIDEO_ENCODER_OUTPUT_METADATA
dev_langs:
 - c++
---

## -description

Represents metadata about an [ID3D12VideoEncodeCommandList2::EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) operation.

## -struct-fields

### -field EncodeErrorFlags

A **UINT64** representing a bitwise OR combination of values from the [D3D12_VIDEO_ENCODER_ENCODE_ERROR_FLAG](ne-d3d12video-d3d12_video_encoder_encode_error_flags.md) enumeration specifying information about the encode execution status. 

### -field EncodeStats

A [D3D12_VIDEO_ENCODER_OUTPUT_METADATA_STATISTICS](ns-d3d12video-d3d12_video_encoder_output_metadata_statistics.md) representing statistics for an **EncodeFrame** operation.

### -field EncodedBitstreamWrittenBytesCount

Output field that receives a **UINT64** indicating how many bytes were into [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM.pBuffer](ns-d3d12video-d3d12_video_encoder_compressed_bitstream.md) plus the value of  [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM.FrameStartOffset](ns-d3d12video-d3d12_video_encoder_compressed_bitstream.md).

### -field WrittenSubregionsCount

Output field that receives a **UINT64** indicating the number of subregions used to encode the current frame.

This value is coherent with the settings specified in [D3D12_VIDEO_ENCODER_SEQUENCE_CONTROL_DESC.pFrameSubregionsLayoutData](ns-d3d12video-d3d12_video_encoder_sequence_control_desc.md). If a number of subregions was specified, *WrittenSubregionsCount* should match that value. If another mode was used, this field is how the driver reports the final number of subregions. If the output is a full frame, then there is only 1 subregion.

## -remarks

**D3D12_VIDEO_ENCODER_OUTPUT_METADATA** and its child structures are all aligned to a 64-bit access boundary for use with [SetPredication](../d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication.md).

## -see-also

