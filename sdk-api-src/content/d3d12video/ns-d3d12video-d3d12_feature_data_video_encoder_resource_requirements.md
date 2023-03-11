---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
tech.root: mf
title: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
ms.date: 06/13/2021
targetos: Windows
description: Retrieves values indicating resource requirements for video encoding with the specified encoding configuration.
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_ENCODER_RESOURCE_REQUIREMENTS
dev_langs:
 - c++
---

## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12_FEATURE_VIDEO_ENCODER_RESOURCE_REQUIREMENTS](ne-d3d12video-d3d12_feature_video.md). Retrieves values indicating resource requirements for video encoding with the specified encoding configuration.

## -struct-fields

### -field NodeIndex

In multi-adapter operation, this indicates which physical adapter of the device this operation applies to.

### -field Codec

A member of the [D3D12_VIDEO_ENCODER_CODEC](ne-d3d12video-d3d12_video_encoder_codec.md) enumeration specifying the codec for which resource requirements are being queried.

### -field Profile

A [D3D12_VIDEO_ENCODER_PROFILE_DESC](ns-d3d12video-d3d12_video_encoder_profile_desc.md) structure specifying the profile for which resource requirements are being queried.

### -field InputFormat

A [DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) structure representing the input format for which resource requirements are being queried.

### -field PictureTargetResolution

A [D3D12_VIDEO_ENCODER_PICTURE_RESOLUTION_DESC](ns-d3d12video-d3d12_video_encoder_picture_resolution_desc.md) structure representing the resolution for which resource requirements are being queried.

### -field IsSupported

Receives a boolean value indicating if the specified parameters are supported.

### -field CompressedBitstreamBufferAccessAlignment

Receives a UINT indicating the alignment required in bytes for the resource to be passed in [D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM.pBuffer](ns-d3d12video-d3d12_video_encoder_compressed_bitstream.md) and **D3D12_VIDEO_ENCODER_COMPRESSED_BITSTREAM.Offset**. If no alignment is required, 1 should is returned to indicate 1 byte (trivial) alignment.

### -field EncoderMetadataBufferAccessAlignment

Receives a UINT indicating the alignment required in bytes for the resource to be passed in D3D12_VIDEO_ENCODER_OUTPUT_ARGUMENTS.pEncoderOutputMetadata. If no alignment required, 1 should be reported to convey 1 byte (trivial) alignment.

### -field MaxEncoderOutputMetadataBufferSize

Receives a UINT indicating the maximum size in bytes needed for the [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) that will be allocated by the host and used as output in the [EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md) for output encoder metadata based on the input arguments.

## -remarks

## -see-also

[DXGI_FORMAT](../dxgiformat/ne-dxgiformat-dxgi_format.md)

[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)

[EncodeFrame](nf-d3d12video-id3d12videoencodecommandlist2-encodeframe.md)

