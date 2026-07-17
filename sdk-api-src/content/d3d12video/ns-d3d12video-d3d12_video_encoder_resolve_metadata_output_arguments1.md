---
UID: NS:d3d12video.D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
tech.root: mf
title: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
ms.date: 04/07/2026
targetos: Windows
description: Represents output arguments for ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1, with support for optional metadata outputs.
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
req.typenames: D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
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
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
f1_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
 - d3d12video/D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS1
---

## -description

Represents output arguments for [ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1](nf-d3d12video-id3d12videoencodecommandlist4-resolveencoderoutputmetadata1.md), with support for optional metadata outputs including QP maps, SATD maps, bit allocation maps, and PSNR data.

## -struct-fields

### -field ResolvedLayoutMetadata

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) containing the mandatory resolved metadata. The resolved layout is unchanged from previous versions.

### -field pOutputQPMap

A pointer to an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) texture for QP map output. Can be **NULL** if **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_QP_MAP** is not set. When present, the texture format must be **DXGI_FORMAT_R8_SINT** for H.264 and HEVC, or **DXGI_FORMAT_R8_UINT** for AV1. Dimensions must match *EncoderOutputMetadataQPMapTextureDimensions* from [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements1.md).

### -field pOutputSATDMap

A pointer to an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) texture for SATD map output. Can be **NULL** if **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_SATD_MAP** is not set. When present, the texture format must be **DXGI_FORMAT_R32_UINT**. Dimensions must match *EncoderOutputMetadataSATDMapTextureDimensions* from [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements1.md).

### -field pOutputBitAllocationMap

A pointer to an [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) texture for bit allocation map output. Can be **NULL** if **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_RC_BIT_ALLOCATION_MAP** is not set. When present, the texture format must be **DXGI_FORMAT_R32_UINT**. Dimensions must match *EncoderOutputMetadataBitAllocationMapTextureDimensions* from [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements1.md).

### -field ResolvedFramePSNRData

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) for frame-level PSNR data. The associated **ID3D12Resource** can be **NULL** if **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_FRAME_PSNR** is not set. When present, the resource must be a **D3D12_RESOURCE_DIMENSION_BUFFER** with *Width* set to `sizeof(D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT)`. The contents are interpreted as [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_psnr_resolved_layout.md).

### -field ResolvedSubregionsPSNRData

A [D3D12_VIDEO_ENCODER_ENCODE_OPERATION_METADATA_BUFFER](ns-d3d12video-d3d12_video_encoder_encode_operation_metadata_buffer.md) for subregion-level PSNR data. The associated **ID3D12Resource** can be **NULL** if **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_SUBREGIONS_PSNR** is not set. When present, the resource must be a **D3D12_RESOURCE_DIMENSION_BUFFER** with *Width* matching *EncoderOutputMetadataSubregionsPSNRResolvedMetadataBufferSize* from [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements1.md). The contents are interpreted as a packed array of [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_psnr_resolved_layout.md) with one element per subregion.

## -remarks

This structure extends [D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments.md) with optional metadata outputs.

## -see-also

[ID3D12VideoEncodeCommandList4::ResolveEncoderOutputMetadata1](nf-d3d12video-id3d12videoencodecommandlist4-resolveencoderoutputmetadata1.md)

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_ARGUMENTS](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_arguments.md)

[D3D12_VIDEO_ENCODER_RESOLVE_METADATA_OUTPUT_PSNR_RESOLVED_LAYOUT](ns-d3d12video-d3d12_video_encoder_resolve_metadata_output_psnr_resolved_layout.md)

