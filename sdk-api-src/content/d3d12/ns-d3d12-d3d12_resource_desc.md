---
UID: NS:d3d12.D3D12_RESOURCE_DESC
title: D3D12_RESOURCE_DESC (d3d12.h)
description: Describes a resource, such as a texture. This structure is used extensively.
helpviewer_keywords: ["D3D12_RESOURCE_DESC","D3D12_RESOURCE_DESC structure","d3d12/D3D12_RESOURCE_DESC","direct3d12.d3d12_resource_desc"]
old-location: direct3d12\d3d12_resource_desc.htm
tech.root: direct3d12
ms.assetid: 908BCB65-A7C6-473D-81AB-CCCA029AB6F9
ms.date: 12/05/2018
ms.keywords: D3D12_RESOURCE_DESC, D3D12_RESOURCE_DESC structure, d3d12/D3D12_RESOURCE_DESC, direct3d12.d3d12_resource_desc
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
req.typenames: D3D12_RESOURCE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RESOURCE_DESC
 - d3d12/D3D12_RESOURCE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RESOURCE_DESC
---

# D3D12_RESOURCE_DESC structure

## -description

Describes a resource, such as a texture. This structure is used extensively.

## -struct-fields

### -field Dimension

One member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension">D3D12_RESOURCE_DIMENSION</a>, specifying the dimensions of the resource (for example, D3D12_RESOURCE_DIMENSION_TEXTURE1D), or whether it is a buffer ((D3D12_RESOURCE_DIMENSION_BUFFER).

### -field Alignment

Specifies the alignment.

### -field Width

Specifies the width of the resource.

### -field Height

Specifies the height of the resource.

### -field DepthOrArraySize

Specifies the depth of the resource, if it is 3D, or the array size if it is an array of 1D or 2D resources.

### -field MipLevels

Specifies the number of MIP levels.

### -field Format

Specifies one member of  <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>.

### -field SampleDesc

Specifies a <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a> structure.

### -field Layout

Specifies one member of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout">D3D12_TEXTURE_LAYOUT</a>.

### -field Flags

Bitwise-OR'd flags, as <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags">D3D12_RESOURCE_FLAGS</a> enumeration constants.

## -remarks

Use this structure with:<ul>
<li>
<a href="/windows/desktop/direct3d12/id3d12resource-getdesc">ID3D12Resource::GetDesc</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo(uint_uint_constd3d12_resource_desc)">ID3D12Device::GetResourceAllocationInfo</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource">ID3D12Device::CreateCommittedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource">ID3D12Device::CreatePlacedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource">ID3D12Device::CreateReservedResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints">ID3D12Device::GetCopyableFootprints</a>
</li>
<li>A number of the helper functions, refer to <a href="/windows/desktop/direct3d12/helper-structures-and-functions-for-d3d12">Helper Structures and Functions for D3D12</a>.</li>
</ul>

Two common resources are buffers and textures, which both use this structure, but with quite different uses of the fields.

<h3><a id="Buffers"></a><a id="buffers"></a><a id="BUFFERS"></a>Buffers</h3>
Buffers are a contiguous memory region.
 <i>Width</i> may be between 1 and either the <i>MaxGPUVirtualAddressBitsPerResource</i> field of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support">D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</a> for reserved resources or the <i>MaxGPUVirtualAddressBitsPerProcess</i> field for committed resources. However, exhaustion of GPU virtual address space, memory residency budget (see <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">IDXGIAdapter3::QueryVideoMemoryInfo</a>), and or system memory may easily occur first.

<i>Alignment</i> must be 64KB (D3D12_DEFAULT_RESOURCE_PLACEMENT_ALIGNMENT) or 0, which is effectively 64KB.

<i>Height</i>, <i>DepthOrArraySize</i>, and <i>MipLevels</i> must be 1.

<i>Format</i> must be DXGI_FORMAT_UNKNOWN.

<i>SampleDesc.Count</i> must be 1 and <i>Quality</i> must be 0.

<i>Layout</i> must be D3D12_TEXTURE_LAYOUT_ROW_MAJOR, as buffer memory layouts are understood by applications and row-major texture data is commonly marshaled through buffers.

<i>Flags</i> must still be accurately filled out by applications for buffers, with minor exceptions. However, applications can use the most amount of capability support without concern about the efficiency impact on buffers. The flags field is meant to control properties related to textures.

<h3><a id="Textures"></a><a id="textures"></a><a id="TEXTURES"></a>Textures</h3>
Textures are a multi-dimensional arrangement of texels in a contiguous region of memory, heavily optimized to maximize bandwidth for rendering and sampling. Texture sizes are hard to predict and vary from adapter to adapter. Applications must use <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo(uint_uint_constd3d12_resource_desc)">ID3D12Device::GetResourceAllocationInfo</a> to accurately understand their size.

TEXTURE1D, TEXTURE2D, and TEXTURE3D are not supported orthogonally on every format. See the use of D3D12_FORMAT_SUPPORT1_TEXTURE1D, D3D12_FORMAT_SUPPORT1_TEXTURE2D, and D3D12_FORMAT_SUPPORT1_TEXTURE3D in <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1">D3D12_FORMAT_SUPPORT1</a>.

<i>Width</i>, <i>Height</i>, and <i>DepthOrArraySize</i> must be between 1 and the maximum dimension supported for the particular feature level and texture dimension. However, exhaustion of GPU virtual address space, memory residency budget (see <a href="/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo">IDXGIAdapter3::QueryVideoMemoryInfo</a>), and or system memory may easily occur first. For compressed formats, these dimensions are logical. For example:

<ul>
<li>For TEXTURE1D: <ul>
<li><i>Width</i> must be less than or equal to D3D10_REQ_TEXTURE1D_U_DIMENSION on feature levels less than 11_0 and D3D11_REQ_TEXTURE1D_U_DIMENSION on feature level 11_0 or greater.</li>
<li><i>Height</i> must be 1.</li>
<li><i>DepthOrArraySize</i> is interpreted as array size and must be less than or equal to D3D10_REQ_TEXTURE1D_ARRAY_AXIS_DIMENSION on feature levels less than 11_0 and D3D11_REQ_TEXTURE1D_ARRAY_AXIS_DIMENSION on feature levels 11_0 or greater.</li>
</ul>
</li>
<li>For TEXTURE2D:
 <ul>
<li><i>Width</i> and <i>Height</i> must be less than or equal to D3D10_REQ_TEXTURE2D_U_OR_V_DIMENSION on feature levels less than 11_0 and D3D11_REQ_TEXTURE2D_U_OR_V_DIMENSION or feature level 11_0 or greater.
 </li>
<li><i>DepthOrArraySize</i> is interpreted as array size and must be less than or equal to D3D10_REQ_TEXTURE2D_ARRAY_AXIS_DIMENSION on feature levels less than 11_0 and D3D11_REQ_TEXTURE2D_ARRAY_AXIS_DIMENSION on feature levels 11_0 or greater.</li>
</ul>
</li>
<li>For TEXTURE3D:
 <ul>
<li><i>Width</i> and <i>Height</i> and <i>DepthOrArraySize</i> must be less than or equal to D3D10_REQ_TEXTURE3D_U_V_OR_W_DIMENSION on feature levels less than 11_0 and D3D11_REQ_TEXTURE2D_U_V_OR_W_DIMENSION on feature level 11_0 or greater.
 </li>
<li><i>DepthOrArraySize</i> is interpreted as depth.</li>
</ul>
</li>
</ul>
The following notes are for all texture sizes.

<h3><a id="_____Alignment"></a><a id="_____alignment"></a><a id="_____ALIGNMENT"></a>     Alignment</h3>
<i>Alignment</i> may be one of 0, 4KB, 64KB or 4MB. 

If <i>Alignment</i> is set to 0, the runtime will use 4MB for MSAA textures and 64KB for everything else. The application may choose smaller alignments than these defaults for a couple of texture types when the texture is small.
Textures with UNKNOWN layout and MSAA may be created with 64KB alignment (if they pass the small size restriction detailed below).

Textures with UNKNOWN layout without MSAA and without  render-target nor depth-stencil flags may be created with 4KB Alignment (again, passing the small size restriction).

Applications can create smaller aligned resources when the estimated size of the most-detailed mip level is a total of the larger alignment restriction or less. The runtime will use an architecture-independent mechanism of size-estimation, that mimics the way standard swizzle and D3D12 tiled resources are sized. However, the tile sizes will be of the smaller alignment restriction for such calculations. 
Using the non-render-target and non-depth-stencil texture as an example, the runtime will assume near-equilateral tile shapes of 4KB, and calculate the number of tiles needed for the most-detailed mip level. If the number of tiles is equal to or less than 16, then the application can create a 4KB aligned resource. So, a mipped tex2d array of any array size and any number of mip levels can be 4KB, as long as the width and height are small enough for the particular format and MSAA.

<h3><a id="MipLevels"></a><a id="miplevels"></a><a id="MIPLEVELS"></a>MipLevels</h3>
<i>MipLevels</i> may be 0, or 1 to the maximum mip levels supported by the <i>Width</i>, <i>Height</i> , and <i>DepthOrArraySize</i> dimensions. When 0 is used, the API will automatically calculate the maximum mip levels supported and use that. But, some resource and heap properties preclude mip levels, so the app must specify the value as 1. 

Refer to the D3D12_FORMAT_SUPPORT1_MIP field of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1">D3D12_FORMAT_SUPPORT1</a> for per-format restrictions. MSAA resources, textures with D3D12_RESOURCE_FLAG_ALLOW_CROSS_ADAPTER, and heaps with D3D12_HEAP_FLAG_ALLOW_DISPLAY all preclude mip levels.
  

<h3><a id="Format"></a><a id="format"></a><a id="FORMAT"></a>Format</h3>
<i>Format</i> must be a valid format supported at the feature level of the device.

<h3><a id="SampleDesc"></a><a id="sampledesc"></a><a id="SAMPLEDESC"></a>SampleDesc</h3>
A <i>SampleDesc.Count</i> greater than 1 and/ or non-zero <i>Quality</i> are only supported for TEXTURE2D and when either D3D12_RESOURCE_FLAG_ALLOW_RENDER_TARGET or D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL are set.

 The following are unsupported:

<ul>
<li>D3D12_TEXTURE_LAYOUT_64KB_STANDARD_SWIZZLE, </li>
<li>D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS, </li>
<li>D3D12_RESOURCE_FLAG_ALLOW_SIMULTANEOUS_ACCESS,</li>
<li>D3D12_HEAP_FLAG_ALLOW_DISPLAY</li>
</ul>
See <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels">D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS</a> for determining valid <i>Count</i> and <i>Quality</i> values.

## -see-also

<a href="/windows/desktop/direct3d12/cd3dx12-resource-desc">CD3DX12_RESOURCE_DESC</a>

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>

<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a>
