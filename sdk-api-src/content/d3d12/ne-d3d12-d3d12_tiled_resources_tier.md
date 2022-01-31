---
UID: NE:d3d12.D3D12_TILED_RESOURCES_TIER
title: D3D12_TILED_RESOURCES_TIER (d3d12.h)
description: Identifies the tier level at which tiled resources are supported.
helpviewer_keywords: ["D3D12_TILED_RESOURCES_TIER","D3D12_TILED_RESOURCES_TIER enumeration","D3D12_TILED_RESOURCES_TIER_1","D3D12_TILED_RESOURCES_TIER_2","D3D12_TILED_RESOURCES_TIER_3","D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED","d3d12/D3D12_TILED_RESOURCES_TIER","d3d12/D3D12_TILED_RESOURCES_TIER_1","d3d12/D3D12_TILED_RESOURCES_TIER_2","d3d12/D3D12_TILED_RESOURCES_TIER_3","d3d12/D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED","direct3d12.d3d12_tiled_resources_tier"]
old-location: direct3d12\d3d12_tiled_resources_tier.htm
tech.root: direct3d12
ms.assetid: ADBA96C3-BD9E-4F12-89C8-371F6F7D369D
ms.date: 12/05/2018
ms.keywords: D3D12_TILED_RESOURCES_TIER, D3D12_TILED_RESOURCES_TIER enumeration, D3D12_TILED_RESOURCES_TIER_1, D3D12_TILED_RESOURCES_TIER_2, D3D12_TILED_RESOURCES_TIER_3, D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED, d3d12/D3D12_TILED_RESOURCES_TIER, d3d12/D3D12_TILED_RESOURCES_TIER_1, d3d12/D3D12_TILED_RESOURCES_TIER_2, d3d12/D3D12_TILED_RESOURCES_TIER_3, d3d12/D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED, direct3d12.d3d12_tiled_resources_tier
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
req.typenames: D3D12_TILED_RESOURCES_TIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TILED_RESOURCES_TIER
 - d3d12/D3D12_TILED_RESOURCES_TIER
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
 - D3D12_TILED_RESOURCES_TIER
---

# D3D12_TILED_RESOURCES_TIER enumeration


## -description

Identifies the tier level at which tiled resources are supported.

## -enum-fields

### -field D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED:0

Indicates that textures cannot be created with the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a> layout.
            


<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a> cannot be used, not even for buffers.

### -field D3D12_TILED_RESOURCES_TIER_1:1

Indicates that 2D textures can be created with the D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE layout.
              Limitations exist for certain resource formats and properties.
              For more details, see <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a>.
            


<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a> can be used.
            

GPU reads or writes to NULL mappings are undefined.
              Applications are encouraged to workaround this limitation by repeatedly mapping the same page to everywhere a NULL mapping would've been used.
            

When the size of a texture mipmap level is an integer multiple of the standard tile shape for its format, it is guaranteed to be nonpacked.

### -field D3D12_TILED_RESOURCES_TIER_2:2

Indicates that a superset of Tier_1 functionality is supported, including this additional support:
            

<ul>
<li>When the size of a texture mipmap level is at least one standard tile shape for its format, the mipmap level is guaranteed to be nonpacked.
                For more info, see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info">D3D12_PACKED_MIP_INFO</a>.
              </li>
<li>Shader instructions are available for clamping level-of-detail (LOD) and for obtaining status about the shader operation.
                For info about one of these shader instructions, see Sample(S,float,int,float,uint).
                <a href="/windows/desktop/direct3dhlsl/sample-s-float--int-uint-">Sample(S,float,int,float,uint)</a>.
              </li>
<li>Reading from <b>NULL</b>-mapped tiles treat that sampled value as zero.
                Writes to <b>NULL</b>-mapped tiles are discarded.
              </li>
</ul>
Adapters that support feature level 12_0 all support TIER_2 or greater.

### -field D3D12_TILED_RESOURCES_TIER_3:3

Indicates that a superset of Tier 2 is supported, with the addition that 3D textures (<a href="/windows/desktop/direct3d12/volume-tiled-resources">Volume Tiled Resources</a>) are supported.

### -field D3D12_TILED_RESOURCES_TIER_4:4

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
      

There are three discrete pieces of functionality bundled together for tiled resource functionality:
        

<ul>
<li>A tile-based texture layout option where nearby texel addresses contain nearby data coordinates.
            A tile of texels contains nearly the same amount of texels in each cardinal dimension of the resource.
            This layout is represented in D3D12 by <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a>.
          </li>
<li>Reserve a region of virtual address space for a resource, where each page is initially NULL-mapped.
            In D3D12, this is operation is encapsulated within <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a>,
            which only works with textures that have the D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE layout.
          </li>
<li>The ability to change page mappings and manipulate texture data on tile granularities.
            In D3D12, these operations are
            <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings">ID3D12CommandQueue::UpdateTileMappings</a>,
            <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings">ID3D12CommandQueue::CopyTileMappings</a>, and
            <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles">ID3D12GraphicsCommandList::CopyTiles</a>.
          </li>
</ul>
Three significant changes over D3D11 are:
        

<ul>
<li>Tile pools are replaced by heaps.
            Heaps provide a superset of capabilities than D3D11 tile pools do.
          </li>
<li>Reserved resources may be mapped to pages from multiple heaps at the same time.
            The D3D11 restriction that all non-NULL mapped pages must come from the same heap does not exist.
          </li>
<li>Applications should be aware of GPU virtual address capabilities, which enable litmus tests for particular usage scenarios.
            See <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.
          </li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
