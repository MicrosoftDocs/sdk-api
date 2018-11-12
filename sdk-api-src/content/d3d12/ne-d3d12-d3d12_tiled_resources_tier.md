---
UID: NE:d3d12.D3D12_TILED_RESOURCES_TIER
title: D3D12_TILED_RESOURCES_TIER
author: windows-sdk-content
description: Identifies the tier level at which tiled resources are supported.
old-location: direct3d12\d3d12_tiled_resources_tier.htm
tech.root: direct3d12
ms.assetid: ADBA96C3-BD9E-4F12-89C8-371F6F7D369D
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_TILED_RESOURCES_TIER, D3D12_TILED_RESOURCES_TIER enumeration, D3D12_TILED_RESOURCES_TIER_1, D3D12_TILED_RESOURCES_TIER_2, D3D12_TILED_RESOURCES_TIER_3, D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED, d3d12/D3D12_TILED_RESOURCES_TIER, d3d12/D3D12_TILED_RESOURCES_TIER_1, d3d12/D3D12_TILED_RESOURCES_TIER_2, d3d12/D3D12_TILED_RESOURCES_TIER_3, d3d12/D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED, direct3d12.d3d12_tiled_resources_tier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TILED_RESOURCES_TIER
product: Windows
targetos: Windows
req.typenames: D3D12_TILED_RESOURCES_TIER
req.redist: 
---

# D3D12_TILED_RESOURCES_TIER enumeration


## -description


Identifies the tier level at which tiled resources are supported.
        


## -enum-fields




### -field D3D12_TILED_RESOURCES_TIER_NOT_SUPPORTED

Indicates that textures cannot be created with the <a href="https://msdn.microsoft.com/1C61B658-9CA1-493C-8DBC-86313D0D302F">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a> layout.
            


<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">ID3D12Device::CreateReservedResource</a> cannot be used, not even for buffers.
            


### -field D3D12_TILED_RESOURCES_TIER_1

Indicates that 2D textures can be created with the D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE layout.
              Limitations exist for certain resource formats and properties.
              For more details, see <a href="https://msdn.microsoft.com/1C61B658-9CA1-493C-8DBC-86313D0D302F">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a>.
            


<a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">ID3D12Device::CreateReservedResource</a> can be used.
            

GPU reads or writes to NULL mappings are undefined.
              Applications are encouraged to workaround this limitation by repeatedly mapping the same page to everywhere a NULL mapping would've been used.
            

When the size of a texture mipmap level is an integer multiple of the standard tile shape for its format, it is guaranteed to be nonpacked.
            


### -field D3D12_TILED_RESOURCES_TIER_2

Indicates that a superset of Tier_1 functionality is supported, including this additional support:
            

<ul>
<li>When the size of a texture mipmap level is at least one standard tile shape for its format, the mipmap level is guaranteed to be nonpacked.
                For more info, see <a href="https://msdn.microsoft.com/B9231C70-A6FF-4660-90B8-04207D2FF762">D3D12_PACKED_MIP_INFO</a>.
              </li>
<li>Shader instructions are available for clamping level-of-detail (LOD) and for obtaining status about the shader operation.
                For info about one of these shader instructions, see Sample(S,float,int,float,uint).
                <a href="https://msdn.microsoft.com/1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F">Sample(S,float,int,float,uint)</a>.
              </li>
<li>Reading from <b>NULL</b>-mapped tiles treat that sampled value as zero.
                Writes to <b>NULL</b>-mapped tiles are discarded.
              </li>
</ul>
Adapters that support feature level 12_0 all support TIER_2 or greater.
            


### -field D3D12_TILED_RESOURCES_TIER_3

Indicates that a superset of Tier 2 is supported, with the addition that 3D textures (<a href="https://msdn.microsoft.com/F670D15D-BC0F-4F90-99C1-A35192FE8980">Volume Tiled Resources</a>) are supported.
          


### -field D3D12_TILED_RESOURCES_TIER_4




## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/3193E3CC-C6CA-43D4-8D8C-41B7FCEE2BDF">D3D12_FEATURE_DATA_D3D12_OPTIONS</a> structure.
      

There are three discrete pieces of functionality bundled together for tiled resource functionality:
        

<ul>
<li>A tile-based texture layout option where nearby texel addresses contain nearby data coordinates.
            A tile of texels contains nearly the same amount of texels in each cardinal dimension of the resource.
            This layout is represented in D3D12 by <a href="https://msdn.microsoft.com/1C61B658-9CA1-493C-8DBC-86313D0D302F">D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE</a>.
          </li>
<li>Reserve a region of virtual address space for a resource, where each page is initially NULL-mapped.
            In D3D12, this is operation is encapsulated within <a href="https://msdn.microsoft.com/37E74129-1B5C-4997-A584-D7E9F92342EA">ID3D12Device::CreateReservedResource</a>,
            which only works with textures that have the D3D12_TEXTURE_LAYOUT_64KB_UNDEFINED_SWIZZLE layout.
          </li>
<li>The ability to change page mappings and manipulate texture data on tile granularities.
            In D3D12, these operations are
            <a href="https://msdn.microsoft.com/8A8017E5-AB55-4660-855B-D6F93F69CB52">ID3D12CommandQueue::UpdateTileMappings</a>,
            <a href="https://msdn.microsoft.com/FAFA4B5C-EA3C-4209-AB8E-75F3B90F3745">ID3D12CommandQueue::CopyTileMappings</a>, and
            <a href="https://msdn.microsoft.com/F770CE6B-DD70-4102-BEFD-3E46B9957F5E">ID3D12GraphicsCommandList::CopyTiles</a>.
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
            See <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT</a>.
          </li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

