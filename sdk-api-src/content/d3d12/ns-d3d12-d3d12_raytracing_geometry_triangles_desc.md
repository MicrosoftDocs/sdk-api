---
UID: NS:d3d12.D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC
title: D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC (d3d12.h)
description: Describes a set of triangles used as raytracing geometry. The geometry pointed to by this struct are always in triangle list form, indexed or non-indexed. Triangle strips are not supported.
helpviewer_keywords: ["D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC","D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC structure","PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC","PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC structure pointer","d3d12/D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC","d3d12/PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC","direct3d12.d3d12_raytracing_geometry_triangles_desc"]
old-location: direct3d12\d3d12_raytracing_geometry_triangles_desc.htm
tech.root: direct3d12
ms.assetid: 21F4FE2C-FE1B-4520-BEE7-5058467B54D1
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC, D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC structure, PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC, PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC structure pointer, d3d12/D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC, d3d12/PD3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC, direct3d12.d3d12_raytracing_geometry_triangles_desc
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
req.typenames: D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC
 - d3d12/D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC
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
 - D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC
---

# D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC structure


## -description

Describes a set of triangles used as raytracing geometry. The geometry pointed to by this struct are always in triangle list form, indexed or non-indexed. Triangle strips are not supported.

## -struct-fields

### -field Transform3x4

Address of a 3x4 affine transform matrix in row-major layout to be applied to the vertices in the <i>VertexBuffer</i> during an acceleration structure build.  The contents of <i>VertexBuffer</i> are not modified.  If a 2D vertex format is used, the transformation is applied with the third vertex component assumed to be zero. 

If <i>Transform3x4</i> is NULL the vertices will not be transformed. Using <i>Transform3x4</i> may result in increased computation and/or memory requirements for the acceleration structure build.


The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  The address must be aligned to 16 bytes, defined as <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_TRANSFORM3X4_BYTE_ALIGNMENT</a>.

### -field IndexFormat

Format of the indices in the <i>IndexBuffer</i>.  Must be one of the following:

<ul>
<li><b>DXGI_FORMAT_UNKNOWN</b> - when IndexBuffer is NULL</li>
<li><b>DXGI_FORMAT_R32_UINT</b></li>
<li><b>DXGI_FORMAT_R16_UINT</b></li>
</ul>

### -field VertexFormat

Format of the vertices in <i>VertexBuffer</i>.  Must be one of the following:

<ul>
<li><b>DXGI_FORMAT_R32G32_FLOAT</b> - third component is assumed 0</li>
<li><b>DXGI_FORMAT_R32G32B32_FLOAT</b></li>
<li><b>DXGI_FORMAT_R16G16_FLOAT</b> - third component is assumed 0</li>
<li><b>DXGI_FORMAT_R16G16B16A16_FLOAT</b>  - A16 component is ignored, other data can be packed there, such as setting vertex stride to 6 bytes.</li>
<li><b>DXGI_FORMAT_R16G16_SNORM</b>  - third component is assumed 0</li>
<li><b>DXGI_FORMAT_R16G16B16A16_SNORM</b>   - A16 component is ignored, other data can be packed there, such as setting vertex stride to 6 bytes.</li>
</ul>

Tier 1.1 devices support the following additional formats:
<ul>
<li><b>DXGI_FORMAT_R16G16B16A16_UNORM</b>   - A16 component is ignored, other data can be packed there, such as setting vertex stride to 6 bytes</li>
<li><b>DXGI_FORMAT_R16G16_UNORM</b>   - third component assumed 0</li>
<li><b>DXGI_FORMAT_R10G10B10A2_UNORM</b>   - A2 component is ignored, stride must be 4 bytes</li>
<li><b>DXGI_FORMAT_R8G8B8A8_UNORM</b>   - A8 component is ignored, other data can be packed there, such as setting vertex stride to 3 bytes</li>
<li><b>DXGI_FORMAT_R8G8_UNORM</b>   - third component assumed 0</li>
<li><b>DXGI_FORMAT_R8G8B8A8_SNORM</b>  - A8 component is ignored, other data can be packed there, such as setting vertex stride to 3 bytes</li>
<li><b>DXGI_FORMAT_R8G8_SNORM</b>   - third component assumed 0</li>
</ul>

### -field IndexCount

Number of indices in <i>IndexBuffer</i>.  Must be 0 if <i>IndexBuffer</i> is NULL.

### -field VertexCount

Number of vertices in <i>VertexBuffer</i>.

### -field IndexBuffer

Array of vertex indices.  If NULL, triangles are non-indexed.  Just as with graphics, the address must be aligned to the size of <i>IndexFormat</i>.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  Note that if an app wants to share index buffer inputs between graphics input assembler and raytracing acceleration structure build input, it can always put a resource into a combination of read states simultaneously, e.g. <b>D3D12_RESOURCE_STATE_INDEX_BUFFER</b> | <b>D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</b>.

### -field VertexBuffer

Array of vertices including a stride.  The alignment on the address and stride must be a multiple of the component size, so 4 bytes for formats with 32bit components and 2 bytes for formats with 16bit components.  Unlike graphics, there is no constraint on the stride, other than that the bottom 32bits of the value are all that are used – the field is UINT64 purely to make neighboring fields align cleanly/obviously everywhere.  Each vertex position is expected to be at the start address of the stride range and any excess space is ignored by acceleration structure builds.  This excess space might contain other app data such as vertex attributes, which the app is responsible for manually fetching in shaders, whether it is interleaved in vertex buffers or elsewhere.

The memory pointed to must be in state <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</a>.  Note that if an app wants to share vertex buffer inputs between graphics input assembler and raytracing acceleration structure build input, it can always put a resource into a combination of read states simultaneously, e.g. <b>D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER</b> | <b>D3D12_RESOURCE_STATE_NON_PIXEL_SHADER_RESOURCE</b>
