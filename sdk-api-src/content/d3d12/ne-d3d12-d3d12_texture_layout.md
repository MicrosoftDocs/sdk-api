---
UID: NE:d3d12.D3D12_TEXTURE_LAYOUT
title: D3D12_TEXTURE_LAYOUT (d3d12.h)
description: Specifies texture layout options.
helpviewer_keywords: ["D3D12_TEXTURE_LAYOUT","D3D12_TEXTURE_LAYOUT enumeration","D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE","D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE","D3D12_TEXTURE_LAYOUT_ROW_MAJOR","D3D12_TEXTURE_LAYOUT_UNKNOWN","d3d12/D3D12_TEXTURE_LAYOUT","d3d12/D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE","d3d12/D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE","d3d12/D3D12_TEXTURE_LAYOUT_ROW_MAJOR","d3d12/D3D12_TEXTURE_LAYOUT_UNKNOWN","direct3d12.d3d12_texture_layout"]
old-location: direct3d12\d3d12_texture_layout.htm
tech.root: direct3d12
ms.assetid: 1C61B658-9CA1-493C-8DBC-86313D0D302F
ms.date: 12/05/2018
ms.keywords: D3D12_TEXTURE_LAYOUT, D3D12_TEXTURE_LAYOUT enumeration, D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE, D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE, D3D12_TEXTURE_LAYOUT_ROW_MAJOR, D3D12_TEXTURE_LAYOUT_UNKNOWN, d3d12/D3D12_TEXTURE_LAYOUT, d3d12/D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE, d3d12/D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE, d3d12/D3D12_TEXTURE_LAYOUT_ROW_MAJOR, d3d12/D3D12_TEXTURE_LAYOUT_UNKNOWN, direct3d12.d3d12_texture_layout
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_TEXTURE_LAYOUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEXTURE_LAYOUT
 - d3d12/D3D12_TEXTURE_LAYOUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEXTURE_LAYOUT
---

# D3D12_TEXTURE_LAYOUT enumeration

## -description

Specifies texture layout options.

## -enum-fields

### -field D3D12_TEXTURE_LAYOUT_UNKNOWN:0

Indicates that the layout is unknown, and is likely adapter-dependent.
During creation, the driver chooses the most efficient layout based on other resource properties, especially resource size and flags.
Prefer this choice unless certain functionality is required from another texture layout.

Zero-copy texture upload optimizations exist for UMA architectures; see <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12resource-writetosubresource">ID3D12Resource::WriteToSubresource</a>.

### -field D3D12_TEXTURE_LAYOUT_ROW_MAJOR:1

Indicates that data for the texture is stored in row-major order (sometimes called "pitch-linear order").

This texture layout locates consecutive texels of a row contiguously in memory, before the texels of the next row.
Similarly, consecutive texels of a particular depth or array slice are contiguous in memory before the texels of the next depth or array slice.
Padding may exist between rows and between depth or array slices to align collections of data.
A stride is the distance in memory between rows, depth, or array slices; and it includes any padding.

This texture layout enables sharing of the texture data between multiple adapters, when other layouts aren't available.

Many restrictions apply, because this layout is generally not efficient for extensive usage:

<ul>
<li>The locality of nearby texels is not rotationally invariant.</li>
<li>Only the following texture properties are supported:
<ul>
<li><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>_TEXTURE_2D.</li>
<li>A single mip level.</li>
<li>A single array slice.</li>
<li>64KB alignment.</li>
<li>Non-MSAA.</li>
<li>No <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG</a>_ALLOW_DEPTH_STENCIL.</li>
<li>The format cannot be a YUV format.</li>
</ul>
</li>
<li>The texture must be created on a heap with <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAG</a>_SHARED_CROSS_ADAPTER.</li>
</ul>
Buffers are created with <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT</a>_ROW_MAJOR, because row-major texture data can be located in them without creating a texture object.
This is commonly used for uploading or reading back texture data, especially for discrete/NUMA adapters.
However, <b>D3D12_TEXTURE_LAYOUT</b>_ROW_MAJOR can also be used when marshaling texture data between GPUs or adapters.
For examples of usage with <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion">ID3D12GraphicsCommandList::CopyTextureRegion</a>, see some of the following topics:

<ul>
<li><a href="/windows/win32/direct3d12/default-texture-mapping">Default Texture Mapping and Standard Swizzle</a></li>
<li><a href="/windows/win32/direct3d12/predication">Predication</a></li>
<li><a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a></li>
<li><a href="/windows/win32/direct3d12/upload-and-readback-of-texture-data">Uploading Texture Data</a></li>
</ul>

### -field D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE:2

Indicates that the layout within 64KB tiles and tail mip packing is up to the driver.
No standard swizzle pattern.

This texture layout is arranged into contiguous 64KB regions, also known as tiles, containing near equilateral amount of consecutive number of texels along each dimension.
Tiles are arranged in row-major order.
While there is no padding between tiles, there are typically unused texels within the last tile in each dimension.
The layout of texels within the tile is undefined.
Each subresource immediately follows where the previous subresource end, and the subresource order follows the same sequence as subresource ordinals.
However, tail mip packing is adapter-specific.
For more details, see tiled resource tier and <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-getresourcetiling">ID3D12Device::GetResourceTiling</a>.

This texture layout enables partially resident or sparse texture scenarios when used together with virtual memory page mapping functionality.
This texture layout must be used together with <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a> to enable the usage of <a href="/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">ID3D12CommandQueue::UpdateTileMappings</a>.

Some restrictions apply to textures with this layout:

<ul>
<li>The adapter must support <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier">D3D12_TILED_RESOURCES_TIER</a> 1 or greater.</li>
<li>64KB alignment must be used.</li>
<li><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>_TEXTURE1D is not supported, nor are all formats.</li>
<li>The tiled resource tier indicates whether textures with <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>_TEXTURE3D is supported.</li>
</ul>

### -field D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE:3

Indicates that a default texture uses the standardized swizzle pattern.

This texture layout is arranged the same way that D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE is, except that the layout of texels within the tile is defined. Tail mip packing is adapter-specific.

This texture layout enables optimizations when marshaling data between multiple adapters or between the CPU and GPU.
The amount of copying can be reduced when multiple components understand the texture memory layout.
This layout is generally more efficient for extensive usage than row-major layout, due to the rotationally invariant locality of neighboring texels.
This layout can typically only be used with adapters that support standard swizzle, but exceptions exist for cross-adapter shared heaps.

The restrictions for this layout are that the following aren't supported:
            
<ul>
<li><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>_TEXTURE1D</li>
<li>Multi-sample anti-aliasing (MSAA)</li>
<li><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAG</a>_ALLOW_DEPTH_STENCIL</li>
<li>Formats within the <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>_R32G32B32_TYPELESS group</li>
</ul>

## -remarks

This enum is used by the <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> structure.

This enumeration controls the swizzle pattern of default textures and enable map support on default textures.
Callers must query <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> to ensure that each option is supported.

The standard swizzle formats applies within each page-sized chunk, and pages are laid out in linear order with respect to one another.
A 16-bit interleave pattern defines the conversion from pre-swizzled intra-page location to the post-swizzled location.

<img alt="Standard swizzle patterns" src="./images/d3d12_standardswizzle.png"/>

To demonstrate, consider the 2D 32bpp swizzle format above.
This is represented by the following interleave masks, where bits on the left are most-significant:

``` syntax
UINT xBytesMask = 1010 1010 1000 1111
UINT yMask =      0101 0101 0111 0000
```

To compute the swizzled address, the following code could be used (where the <b>_pdep_u32</b> intrinsic instruction is supported):

``` syntax
UINT swizzledOffset = resourceBaseOffset +
                      _pdep_u32(xOffset, xBytesMask) +
                      _pdep_u32(yOffset, yBytesMask);
```

## -see-also

<a href="/windows/win32/direct3d12/cd3dx12-resource-desc">CD3DX12_RESOURCE_DESC</a>

<a href="/windows/win32/direct3d12/direct3d-12-enumerations">Core Enumerations</a>

<a href="/windows/win32/direct3d12/default-texture-mapping">UMA Optimizations: CPU Accessible Textures and Standard Swizzle</a>
