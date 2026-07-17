---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
ms.date: 04/07/2026
targetos: Windows
description: Retrieves resource requirements for video encoding, with support for optional metadata.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
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
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
dev_langs:
 - c++
helpviewer_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1
---

## -description

Retrieves resource requirements for video encoding, with support for optional metadata. Used with [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) and the **D3D12_FEATURE_VIDEO_ENCODER_RESOURCE_REQUIREMENTS1** feature value.

## -struct-fields

### -field NodeIndex

For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (one of the device's physical adapters) to which the command queue applies. Each bit in the mask corresponds to a single node. Only one bit must be set.

### -field Codec

A [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) specifying the codec to query.

### -field Profile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) specifying the encoder profile.

### -field InputFormat

A [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) specifying the input format.

### -field PictureTargetResolution

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) specifying the target resolution.

### -field IsSupported

Output. Indicates whether the configuration is supported.

### -field CompressedBitstreamBufferAccessAlignment

Output. The required alignment for the compressed bitstream buffer.

### -field EncoderMetadataBufferAccessAlignment

Output. The required alignment for the encoder metadata buffer.

### -field MaxEncoderOutputMetadataBufferSize

Output. The maximum size in bytes of the encoder output metadata buffer.

### -field OptionalMetadata

A [D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAGS](ne-d3d12video-d3d12_video_encoder_optional_metadata_enable_flags.md) value indicating which optional metadata is requested.

### -field CodecConfiguration

A [D3D12_VIDEO_ENCODER_CODEC_CONFIGURATION](ns-d3d12video-d3d12_video_encoder_codec_configuration.md) specifying the codec configuration. Required when any flags are set in *OptionalMetadata*; otherwise pass as zeroed/NULL.

### -field EncoderOutputMetadataQPMapTextureDimensions

Output. A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) indicating the texture dimensions for the QP map output. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_QP_MAP** is set. The block size can be derived by dividing *PictureTargetResolution* by these dimensions.

### -field EncoderOutputMetadataSATDMapTextureDimensions

Output. A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) indicating the texture dimensions for the SATD map output. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_SATD_MAP** is set. The block size can be derived by dividing *PictureTargetResolution* by these dimensions.

### -field EncoderOutputMetadataBitAllocationMapTextureDimensions

Output. A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) indicating the texture dimensions for the bit allocation map output. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_RC_BIT_ALLOCATION_MAP** is set. The block size can be derived by dividing *PictureTargetResolution* by these dimensions.

### -field EncoderOutputMetadataFramePSNRComponentsNumber

Output. The number of PSNR components (Y, U, and V in that order) written for frame-level PSNR. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_FRAME_PSNR** is set.

### -field EncoderOutputMetadataSubregionsPSNRComponentsNumber

Output. The number of PSNR components (Y, U, and V in that order) written per subregion. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_SUBREGIONS_PSNR** is set.

### -field EncoderOutputMetadataSubregionsPSNRResolvedMetadataBufferSize

Output. The required *Width* size of the buffer for subregion PSNR data. Valid when **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_SUBREGIONS_PSNR** is set.

## -remarks

When *OptionalMetadata* is **D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAG_NONE**, the outputs that are also present in [D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements.md) must report identical values for backward compatibility. Output fields for non-selected optional metadata flags are reported as zero.

## -see-also

[D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS](ns-d3d12video-d3d12_feature_data_video_encoder_resource_requirements.md)

[D3D12_VIDEO_ENCODER_OPTIONAL_METADATA_ENABLE_FLAGS](ne-d3d12video-d3d12_video_encoder_optional_metadata_enable_flags.md)

