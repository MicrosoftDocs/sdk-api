---
UID: NE:d3d12.D3D12_HEAP_FLAGS
title: D3D12_HEAP_FLAGS
author: windows-sdk-content
description: Specifies heap options, such as whether the heap can contain textures, and whether resources are shared across adapters.
old-location: direct3d12\d3d12_heap_flags.htm
old-project: direct3d12
ms.assetid: C3C1B611-714C-49DB-8034-9C9B7D6772E4
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_HEAP_FLAGS, D3D12_HEAP_FLAGS enumeration, D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES, D3D12_HEAP_FLAG_ALLOW_DISPLAY, D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS, D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES, D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES, D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH, D3D12_HEAP_FLAG_DENY_BUFFERS, D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES, D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES, D3D12_HEAP_FLAG_HARDWARE_PROTECTED, D3D12_HEAP_FLAG_NONE, D3D12_HEAP_FLAG_SHARED, D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER, d3d12/D3D12_HEAP_FLAGS, d3d12/D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_DISPLAY, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH, d3d12/D3D12_HEAP_FLAG_DENY_BUFFERS, d3d12/D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_HARDWARE_PROTECTED, d3d12/D3D12_HEAP_FLAG_NONE, d3d12/D3D12_HEAP_FLAG_SHARED, d3d12/D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER, direct3d12.d3d12_heap_flags
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
req.typenames: D3D12_HEAP_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_HEAP_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_HEAP_FLAGS enumeration


## -description



          Specifies heap options, such as whether the heap can contain textures, and whether resources are shared across adapters.
        


## -enum-fields




### -field D3D12_HEAP_FLAG_NONE


            No options are specified.
          


### -field D3D12_HEAP_FLAG_SHARED


            The heap is shared. Refer to <a href="https://msdn.microsoft.com/67C6B1D4-BF76-45A9-BADC-7C9520C900EB">Shared Heaps</a>.


### -field D3D12_HEAP_FLAG_DENY_BUFFERS


            The heap isn't allowed to contain buffers.
          


### -field D3D12_HEAP_FLAG_ALLOW_DISPLAY


            The heap is allowed to contain swap-chain surfaces.
           


### -field D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER


            The heap is allowed to share resources across adapters. Refer to <a href="https://msdn.microsoft.com/67C6B1D4-BF76-45A9-BADC-7C9520C900EB">Shared Heaps</a>.
          


### -field D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES


            The heap is not allowed to store Render Target (RT) and/or Depth-Stencil (DS) textures.
          


### -field D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES

The heap is not allowed to contain resources with D3D12_RESOURCE_DIMENSION_TEXTURE1D, D3D12_RESOURCE_DIMENSION_TEXTURE2D, or D3D12_RESOURCE_DIMENSION_TEXTURE3D  unless either D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL are present. Refer to <a href="https://msdn.microsoft.com/E04F3124-01FB-4EE7-BDF8-4821F2F1FCEB">D3D12_RESOURCE_DIMENSION</a> and <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAGS</a>.


### -field D3D12_HEAP_FLAG_HARDWARE_PROTECTED

Unsupported. Do not use.


### -field D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH

The heap supports MEM_WRITE_WATCH functionality, which causes the system to track the pages that are written to in the commited memory region. This flag can't be combined with the D3D12_HEAP_TYPE_DEFAULT or D3D12_CPU_PAGE_PROPERTY_UNKNOWN flags.
	  Applications are discouraged from using this flag themselves because it prevents tools from using this functionality.


### -field D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS


### -field D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES


            The heap is allowed to store all types of buffers and/or textures.
            This is an alias; for more details, see "Aliases" in the Remarks section.
          


### -field D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS


            The heap is only allowed to store buffers.
            This is an alias; for more details, see "Aliases" in the Remarks section.
          


### -field D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES


            The heap is only allowed to store non-RT, non-DS textures.
            This is an alias; for more details, see "Aliases" in the Remarks section.
          


### -field D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES


            The heap is only allowed to store RT and/or DS textures.
            This is an alias; for more details, see "Aliases" in the Remarks section.
          


## -remarks




          This enum is used by the following API items:
        

<ul>
<li>
<a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">ID3D12Device::CreateHeap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3A473476-F37E-4F01-B121-87E998EE9411">D3D12_HEAP_DESC</a> structure
          </li>
</ul>

          The following heap flags must be used with <a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">ID3D12Device::CreateHeap</a>,
          but will be set automatically for implicit heaps created by <a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">ID3D12Device::CreateCommittedResource</a>.
        


          Adapters that only support <a href="https://msdn.microsoft.com/47C5B30C-BFFE-437A-878B-FE49F8EFFD02">heap tier 1</a> must set two out of the three following flags.
        

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_BUFFERS</td>
<td>
              The heap isn't allowed to contain resources with
              D3D12_RESOURCE_DIMENSION_BUFFER (which is a <a href="https://msdn.microsoft.com/E04F3124-01FB-4EE7-BDF8-4821F2F1FCEB">D3D12_RESOURCE_DIMENSION</a> enumeration constant).
            </td>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES</td>
<td>
              The heap isn't allowed to contain resources with
              D3D12_RESOURCE_DIMENSION_TEXTURE1D,
              D3D12_RESOURCE_DIMENSION_TEXTURE2D, or
              D3D12_RESOURCE_DIMENSION_TEXTURE3D
              together with either
              D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or
              D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL.
              (The latter two items are <a href="https://msdn.microsoft.com/EC9DA05A-D0C0-4642-8E49-9ED98B4F19B4">D3D12_RESOURCE_FLAGS</a> enumeration constants.)
            </td>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES</td>
<td>
              The heap isn't allowed to contain resources with
              D3D12_RESOURCE_DIMENSION_TEXTURE1D,
              D3D12_RESOURCE_DIMENSION_TEXTURE2D, or
              D3D12_RESOURCE_DIMENSION_TEXTURE3D
              unless
              D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET and
              D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL are absent.
            </td>
</tr>
</table>
 

<h3><a id="Aliases"></a><a id="aliases"></a><a id="ALIASES"></a>Aliases</h3>

          Adapters that support <a href="https://msdn.microsoft.com/47C5B30C-BFFE-437A-878B-FE49F8EFFD02">heap tier 2</a> or greater are additionally allowed to set none of the above flags.
          Aliases for these flags are available for applications that prefer thinking only of which resources are supported.
        


          The following aliases exist, so be careful when doing bit-manipulations:
        

<ul>
<li>
            D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES = 0 and is only supported on <a href="https://msdn.microsoft.com/47C5B30C-BFFE-437A-878B-FE49F8EFFD02">heap tier 2</a> and greater.
          </li>
<li>
            D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS = D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES | D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES
          </li>
<li>
            D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES = D3D12_HEAP_FLAG_DENY_BUFFERS | D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES
          </li>
<li>
            D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES = D3D12_HEAP_FLAG_DENY_BUFFERS | D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES
          </li>
</ul>
<h3><a id="Displayable_heaps"></a><a id="displayable_heaps"></a><a id="DISPLAYABLE_HEAPS"></a>Displayable heaps</h3>
Displayable heaps are most commonly created by the swapchain for presentation, to enable scanning out to a monitor.

Displayable heaps are specified with the D3D12_HEAP_FLAG_ALLOW_DISPLAY member of the <b>D3D12_HEAP_FLAGS</b> enum.

Applications may create displayable heaps outside of a swapchain; but cannot actually present with them.
 This flag is not supported by <a href="https://msdn.microsoft.com/DB5DF4B2-4673-4B8D-BDED-9F672A41E7F6">CreateHeap</a> and can only be used with <a href="https://msdn.microsoft.com/FF9E8F11-F2C5-4A96-8E25-140870D15DA9">CreateCommittedResource</a> with D3D12_HEAP_TYPE_DEFAULT. 

Additional restrictions to the  <a href="https://msdn.microsoft.com/908BCB65-A7C6-473D-81AB-CCCA029AB6F9">D3D12_RESOURCE_DESC</a> apply to the resource created with displayable heaps.

<ul>
<li>The format must not only be supported by the device, but must be supported for scan-out. Refer to the use of the   D3D12_FORMAT_SUPPORT1_DISPLAY member of <a href="https://msdn.microsoft.com/D987B228-4BC9-4A07-96A0-A518F8F52B06">D3D12_FORMAT_SUPPORT1</a>.</li>
<li><i>Dimension</i> must be D3D12_RESOURCE_DIMENSION_TEXTURE2D.</li>
<li><i>Alignment</i> must be 0.</li>
<li><i>ArraySize</i> may be either 1 or 2.</li>
<li><i>MipLevels</i> must be 1.</li>
<li><i>SampleDesc</i> must have <i>Count</i> set to 1 and <i>Quality</i> set to 0.</li>
<li><i>Layout</i> must be D3D12_TEXTURE_LAYOUT_UNKNOWN.</li>
<li>D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL and D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER are invalid
flags.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/38E0BA60-2BB0-4AC1-870A-10AB16E4C6E6">CD3DX12_HEAP_DESC</a>



<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>



<a href="https://msdn.microsoft.com/04D3FACF-21EC-45CA-AD9B-78FDCDDC7136">Descriptor Heaps</a>
 

 

