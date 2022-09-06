---
UID: NE:d3d12.D3D12_HEAP_FLAGS
title: D3D12_HEAP_FLAGS (d3d12.h)
description: Specifies heap options, such as whether the heap can contain textures, and whether resources are shared across adapters.
helpviewer_keywords: ["D3D12_HEAP_FLAGS","D3D12_HEAP_FLAGS enumeration","D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES","D3D12_HEAP_FLAG_ALLOW_DISPLAY","D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS","D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES","D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES","D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH","D3D12_HEAP_FLAG_DENY_BUFFERS","D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES","D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES","D3D12_HEAP_FLAG_HARDWARE_PROTECTED","D3D12_HEAP_FLAG_NONE","D3D12_HEAP_FLAG_SHARED","D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER","d3d12/D3D12_HEAP_FLAGS","d3d12/D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES","d3d12/D3D12_HEAP_FLAG_ALLOW_DISPLAY","d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS","d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES","d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES","d3d12/D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH","d3d12/D3D12_HEAP_FLAG_DENY_BUFFERS","d3d12/D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES","d3d12/D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES","d3d12/D3D12_HEAP_FLAG_HARDWARE_PROTECTED","d3d12/D3D12_HEAP_FLAG_NONE","d3d12/D3D12_HEAP_FLAG_SHARED","d3d12/D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER","direct3d12.d3d12_heap_flags"]
old-location: direct3d12\d3d12_heap_flags.htm
tech.root: direct3d12
ms.assetid: C3C1B611-714C-49DB-8034-9C9B7D6772E4
ms.date: 12/05/2018
ms.keywords: D3D12_HEAP_FLAGS, D3D12_HEAP_FLAGS enumeration, D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES, D3D12_HEAP_FLAG_ALLOW_DISPLAY, D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS, D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES, D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES, D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH, D3D12_HEAP_FLAG_DENY_BUFFERS, D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES, D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES, D3D12_HEAP_FLAG_HARDWARE_PROTECTED, D3D12_HEAP_FLAG_NONE, D3D12_HEAP_FLAG_SHARED, D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER, d3d12/D3D12_HEAP_FLAGS, d3d12/D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_DISPLAY, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH, d3d12/D3D12_HEAP_FLAG_DENY_BUFFERS, d3d12/D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES, d3d12/D3D12_HEAP_FLAG_HARDWARE_PROTECTED, d3d12/D3D12_HEAP_FLAG_NONE, d3d12/D3D12_HEAP_FLAG_SHARED, d3d12/D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER, direct3d12.d3d12_heap_flags
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
req.typenames: D3D12_HEAP_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_HEAP_FLAGS
 - d3d12/D3D12_HEAP_FLAGS
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
 - D3D12_HEAP_FLAGS
---

## -description

Specifies heap options, such as whether the heap can contain textures, and whether resources are shared across adapters.

## -enum-fields

### -field D3D12_HEAP_FLAG_NONE:0

No options are specified.

### -field D3D12_HEAP_FLAG_SHARED:0x1

The heap is shared. Refer to <a href="/windows/desktop/direct3d12/shared-heaps">Shared Heaps</a>.

### -field D3D12_HEAP_FLAG_DENY_BUFFERS:0x4

The heap isn't allowed to contain buffers.

### -field D3D12_HEAP_FLAG_ALLOW_DISPLAY:0x8

The heap is allowed to contain swap-chain surfaces.

### -field D3D12_HEAP_FLAG_SHARED_CROSS_ADAPTER:0x20

The heap is allowed to share resources across adapters. Refer to <a href="/windows/desktop/direct3d12/shared-heaps">Shared Heaps</a>.

### -field D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES:0x40

The heap is not allowed to store Render Target (RT) and/or Depth-Stencil (DS) textures.

### -field D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES:0x80

The heap is not allowed to contain resources with D3D12_RESOURCE_DIMENSION_TEXTURE1D, D3D12_RESOURCE_DIMENSION_TEXTURE2D, or D3D12_RESOURCE_DIMENSION_TEXTURE3D  unless either D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL are present. Refer to <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a> and <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAGS</a>.

### -field D3D12_HEAP_FLAG_HARDWARE_PROTECTED:0x100

Unsupported. Do not use.

### -field D3D12_HEAP_FLAG_ALLOW_WRITE_WATCH:0x200

The heap supports MEM_WRITE_WATCH functionality, which causes the system to track the pages that are written to in the committed memory region. This flag can't be combined with the D3D12_HEAP_TYPE_DEFAULT or D3D12_CPU_PAGE_PROPERTY_UNKNOWN flags. Applications are discouraged from using this flag themselves because it prevents tools from using this functionality.

### -field D3D12_HEAP_FLAG_ALLOW_SHADER_ATOMICS:0x400

Ensures that atomic operations will be atomic on this heap's memory, according to components able to see the memory.

Creating a heap with this flag will fail under either of these conditions.
- The heap type is **D3D12_HEAP_TYPE_DEFAULT**, and the heap can be visible on multiple nodes, but the device does *not* support [**D3D12_CROSS_NODE_SHARING_TIER_3**](./ne-d3d12-d3d12_cross_node_sharing_tier.md).
- The heap is CPU-visible, but the heap type is *not* **D3D12_HEAP_TYPE_CUSTOM**.

Note that heaps with this flag might be a limited resource on some systems.

### -field D3D12_HEAP_FLAG_CREATE_NOT_RESIDENT:0x800

The heap is created in a non-resident state and must be made resident using [ID3D12Device::MakeResident](./nf-d3d12-id3d12device-makeresident.md) or [ID3D12Device3::EnqueueMakeResident](./nf-d3d12-id3d12device3-enqueuemakeresident.md).

By default, the final step of heap creation is to make the heap resident, so this flag skips this step and allows the application to decide when to do so.

### -field D3D12_HEAP_FLAG_CREATE_NOT_ZEROED:0x1000

Allows the OS to not zero the heap created. By default, committed resources and heaps are almost always zeroed upon creation. This flag allows this to be elided in some scenarios. However, it doesn't guarantee it. For example, memory coming from other processes still needs to be zeroed for data protection and process isolation. This can lower the overhead of creating the heap.

### -field D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES:0

The heap is allowed to store all types of buffers and/or textures. This is an alias; for more details, see "Aliases" in the Remarks section.

### -field D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS:0xc0

The heap is only allowed to store buffers. This is an alias; for more details, see "Aliases" in the Remarks section.

### -field D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES:0x44

The heap is only allowed to store non-RT, non-DS textures. This is an alias; for more details, see "Aliases" in the Remarks section.

### -field D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES:0x84

The heap is only allowed to store RT and/or DS textures. This is an alias; for more details, see "Aliases" in the Remarks section.

## -remarks

This enum is used by the following API items:

<ul>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">ID3D12Device::CreateHeap</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_desc">D3D12_HEAP_DESC</a> structure
          </li>
</ul>
The following heap flags must be used with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">ID3D12Device::CreateHeap</a>,
          but will be set automatically for implicit heaps created by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>.
        
Adapters that only support <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier">heap tier 1</a> must set two out of the three following flags.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_BUFFERS</td>
<td>The heap isn't allowed to contain resources with
              D3D12_RESOURCE_DIMENSION_BUFFER (which is a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a> enumeration constant).
            </td>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES</td>
<td>The heap isn't allowed to contain resources with
              D3D12_RESOURCE_DIMENSION_TEXTURE1D,
              D3D12_RESOURCE_DIMENSION_TEXTURE2D, or
              D3D12_RESOURCE_DIMENSION_TEXTURE3D
              together with either
              D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or
              D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL.
              (The latter two items are <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAGS</a> enumeration constants.)
            </td>
</tr>
<tr>
<td>D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES</td>
<td>The heap isn't allowed to contain resources with
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
Adapters that support <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier">heap tier 2</a> or greater are additionally allowed to set none of the above flags.
          Aliases for these flags are available for applications that prefer thinking only of which resources are supported.

The following aliases exist, so be careful when doing bit-manipulations:

<ul>
<li>D3D12_HEAP_FLAG_ALLOW_ALL_BUFFERS_AND_TEXTURES = 0 and is only supported on <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier">heap tier 2</a> and greater.
          </li>
<li>D3D12_HEAP_FLAG_ALLOW_ONLY_BUFFERS = D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES | D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES
          </li>
<li>D3D12_HEAP_FLAG_ALLOW_ONLY_NON_RT_DS_TEXTURES = D3D12_HEAP_FLAG_DENY_BUFFERS | D3D12_HEAP_FLAG_DENY_RT_DS_TEXTURES
          </li>
<li>D3D12_HEAP_FLAG_ALLOW_ONLY_RT_DS_TEXTURES = D3D12_HEAP_FLAG_DENY_BUFFERS | D3D12_HEAP_FLAG_DENY_NON_RT_DS_TEXTURES
          </li>
</ul>
<h3><a id="Displayable_heaps"></a><a id="displayable_heaps"></a><a id="DISPLAYABLE_HEAPS"></a>Displayable heaps</h3>
Displayable heaps are most commonly created by the swapchain for presentation, to enable scanning out to a monitor.

Displayable heaps are specified with the D3D12_HEAP_FLAG_ALLOW_DISPLAY member of the <b>D3D12_HEAP_FLAGS</b> enum.

Applications may create displayable heaps outside of a swapchain; but cannot actually present with them.
 This flag is not supported by <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createheap">CreateHeap</a> and can only be used with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">CreateCommittedResource</a> with D3D12_HEAP_TYPE_DEFAULT. 

Additional restrictions to the  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc">D3D12_RESOURCE_DESC</a> apply to the resource created with displayable heaps.

<ul>
<li>The format must not only be supported by the device, but must be supported for scan-out. Refer to the use of the   D3D12_FORMAT_SUPPORT1_DISPLAY member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1">D3D12_FORMAT_SUPPORT1</a>.</li>
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

<a href="/windows/desktop/direct3d12/cd3dx12-heap-desc">CD3DX12_HEAP_DESC</a>

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>

<a href="/windows/desktop/direct3d12/descriptor-heaps">Descriptor Heaps</a>
