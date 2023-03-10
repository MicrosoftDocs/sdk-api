---
UID: NE:d3d12video.D3D12_VIDEO_DECODE_TIER
title: D3D12_VIDEO_DECODE_TIER
description: Specifies the decoding tier of a hardware video decoder, which determines the required format of application-defined textures and buffers.
helpviewer_keywords: ["D3D12_VIDEO_DECODE_TIER","D3D12_VIDEO_DECODE_TIER",""]
tech.root: mf
ms.assetid: a7e84f4d-3aa0-4986-a1da-747bbbd6c889
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_DECODE_TIER, D3D12_VIDEO_DECODE_TIER,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.max-support: 
req.typenames: D3D12_VIDEO_DECODE_TIER
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_DECODE_TIER
 - d3d12video/D3D12_VIDEO_DECODE_TIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_DECODE_TIER
---

# D3D12_VIDEO_DECODE_TIER enumeration


## -description

Specifies the decoding tier of a hardware video decoder, which determines the required format of application-defined textures and buffers.

## -enum-fields

### -field D3D12_VIDEO_DECODE_TIER_NOT_SUPPORTED 

Video decoding is not supported.

### -field D3D12_VIDEO_DECODE_TIER_1 

In tier 1, the hardware decoder requires that the application allocate reference textures as a texture array. This is to accommodate hardware requirements that the textures be "close" in address space because the hardware doesn't support a full size pointer for each individual picture buffer.  Instead it has one pointer and a more limited bit offset. For more information on texture arrays, see [Introduction To Textures in Direct3D 11](/windows/win32/direct3d11/overviews-direct3d-11-resources-textures-intro).

If the decoder hardware requires a unique memory layout that is not supported for operations on other engines or different video operations, the decoder may set the <a href="ne-d3d12video-d3d12_video_decode_configuration_flags.md">D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_REFERENCE_ONLY_ALLOCATIONS_REQUIRED</a> configuration flag in the <a href="ns-d3d12video-d3d12_feature_data_video_decode_support.md">D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT</a> structure when queried for profile support. This flag indicates that the application must allocate references with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY</a> flag.  The application should use the <a href="ns-d3d12video-d3d12_video_decode_conversion_arguments.md">D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS</a> structure to set a reference-only output if the output is needed as a future reference frame.  The output frame passed to <a href="nf-d3d12video-id3d12videodecodecommandlist-decodeframe.md">ID3D12VideoCommandList::DecodeFrame</a> is a D3D12 resource that can be consumed by other portions of the pipeline and must not have the D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY flag.

#### Tier 1 requirements for compressed input buffers
- All slices for a given frame must be placed in order and must be contiguous, i.e. there must be no gaps between slices.  Slice control buffers must specify offset and size parameters that meet this requirement.  
- The first slice must begin on a 128 Byte boundary.  The offset set in the <a href="ns-d3d12video-d3d12_video_decode_compressed_bitstream.md">D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM</a> structure must be a multiple of 128 Bytes.
- Decoding is supported from buffers allocated with <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL_L0</a>. This is always system memory, but still a D3D12 buffer.
- Decoding is supported from buffers allocated with D3D12_MEMORY_POOL_L1, the default pool, including those allocated with D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE.

### -field D3D12_VIDEO_DECODE_TIER_2 

In decode tier 2, textures can be referenced as a texture array or as an array of separate texture 2D resources (each resource having array size of 1). This is more flexible for the caller and is important in scenarios where the resolution changes frequently such as in streaming video, because a texture array can only be allocated and deallocated as a single unit, but separate texture 2D resources can be allocated and deallocated individually.  

If decode hardware requires a unique tiling format that is not supported for operations on other engines or different video operations, the decoder may set the <a href="ne-d3d12video-d3d12_video_decode_configuration_flags.md">D3D12_VIDEO_DECODE_CONFIGURATION_FLAG_REFERENCE_ONLY_ALLOCATIONS_REQUIRED</a> configuration flag in the <a href="ns-d3d12video-d3d12_feature_data_video_decode_support.md">D3D12_FEATURE_DATA_VIDEO_DECODE_SUPPORT</a> structure when queried for profile support. This flag indicates that the application must allocate references with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY</a> flag.  The application should use the <a href="ns-d3d12video-d3d12_video_decode_conversion_arguments.md">D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS</a> structure to set a reference only output if the output is needed as a future reference frame.  The output frame passed to <a href="nf-d3d12video-id3d12videodecodecommandlist-decodeframe.md">ID3D12VideoCommandList::DecodeFrame</a> is a D3D12 resource that can be consumed by other portions of the pipeline and must not have the D3D12_RESOURCE_FLAG_VIDEO_DECODE_REFERENCE_ONLY flag.

#### Tier 2 requirements for compressed input buffers

These requirements are identical to the tier 1 requirements.

- All slices for a given frame must be placed in order and must be contiguous, i.e. there must be no gaps between slices.  Slice control buffers must specify offset and size parameters that meet this requirement.  
- The first slice must begin on a 128 Byte boundary.  The offset set in the <a href="ns-d3d12video-d3d12_video_decode_compressed_bitstream.md">D3D12_VIDEO_DECODE_COMPRESSED_BITSTREAM</a> structure must be a multiple of 128 Bytes.
- Decoding is supported from buffers allocated with <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_memory_pool">D3D12_MEMORY_POOL_L0</a>. This is always system memory, but still a D3D12 buffer.
- Decoding is supported from buffers allocated with D3D12_MEMORY_POOL_L1, the default pool, including those allocated with D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE. 
-

### -field D3D12_VIDEO_DECODE_TIER_3 

This field is reserved.

## -remarks

## -see-also