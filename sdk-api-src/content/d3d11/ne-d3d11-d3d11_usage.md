---
UID: NE:d3d11.D3D11_USAGE
title: D3D11_USAGE (d3d11.h)
description: Identifies expected resource use during rendering. The usage directly reflects whether a resource is accessible by the CPU and/or the graphics processing unit (GPU).
helpviewer_keywords: ["7ab4ccb7-1e59-6a38-2ca4-dd87773c596d","D3D11_USAGE","D3D11_USAGE enumeration [Direct3D 11]","D3D11_USAGE_DEFAULT","D3D11_USAGE_DYNAMIC","D3D11_USAGE_IMMUTABLE","D3D11_USAGE_STAGING","d3d11/D3D11_USAGE","d3d11/D3D11_USAGE_DEFAULT","d3d11/D3D11_USAGE_DYNAMIC","d3d11/D3D11_USAGE_IMMUTABLE","d3d11/D3D11_USAGE_STAGING","direct3d11.d3d11_usage"]
old-location: direct3d11\d3d11_usage.htm
tech.root: direct3d11
ms.assetid: 251d462e-964e-42db-8554-dba8f5a9b1ef
ms.date: 12/05/2018
ms.keywords: 7ab4ccb7-1e59-6a38-2ca4-dd87773c596d, D3D11_USAGE, D3D11_USAGE enumeration [Direct3D 11], D3D11_USAGE_DEFAULT, D3D11_USAGE_DYNAMIC, D3D11_USAGE_IMMUTABLE, D3D11_USAGE_STAGING, d3d11/D3D11_USAGE, d3d11/D3D11_USAGE_DEFAULT, d3d11/D3D11_USAGE_DYNAMIC, d3d11/D3D11_USAGE_IMMUTABLE, d3d11/D3D11_USAGE_STAGING, direct3d11.d3d11_usage
req.header: d3d11.h
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
req.typenames: D3D11_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_USAGE
 - d3d11/D3D11_USAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_USAGE
---

# D3D11_USAGE enumeration


## -description

Identifies expected resource use during rendering. The usage directly reflects whether a resource is accessible by the CPU and/or the graphics processing unit (GPU).

## -enum-fields

### -field D3D11_USAGE_DEFAULT:0

A resource that requires read and write access by the GPU. This is likely to be the most common usage choice.

### -field D3D11_USAGE_IMMUTABLE:1

A resource that can only be read by the GPU. It cannot be written by the GPU, and cannot be accessed at all by the CPU. This type of resource must be initialized when it is created, since it cannot be changed after creation.

### -field D3D11_USAGE_DYNAMIC:2

A resource that is accessible by both the GPU (read only) and the CPU (write only). A dynamic resource is a good choice for a resource that will be updated by the CPU at least once per frame. To update a dynamic resource, use a <b>Map</b> method.

For info about how to use dynamic resources, see <a href="/windows/desktop/direct3d11/how-to--use-dynamic-resources">How to: Use dynamic resources</a>.

### -field D3D11_USAGE_STAGING:3

A resource that supports data transfer (copy) from the GPU to the CPU.

## -remarks

An application identifies the way a resource is intended to be used (its usage) in a resource description. There are several structures for creating resources including: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture1d_desc">D3D11_TEXTURE1D_DESC</a>, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture2d_desc">D3D11_TEXTURE2D_DESC</a>, <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_texture3d_desc">D3D11_TEXTURE3D_DESC</a>, and <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10/11:

In Direct3D 9, you specify the type of memory a resource should be created in at resource creation time (using D3DPOOL). It was an application's job to decide what memory pool would provide the best combination of functionality and performance.

In Direct3D 10/11, an application no longer specifies what type of memory (the pool) to create a resource in. Instead, you specify the intended usage of the resource, and let the runtime (in concert with the driver and a memory manager) choose the type of memory that will achieve the best performance.

</td>
</tr>
</table>
 

<h3><a id="Restrictions"></a><a id="restrictions"></a><a id="RESTRICTIONS"></a>Resource Usage Restrictions</h3>
Each usage dictates a tradeoff between accessibility for the CPU and accessibility for the GPU. In general, higher-performance access for one of these two processors means lower-performance access for the other. At either extreme are the <b>D3D11_USAGE_DEFAULT</b> and <b>D3D11_USAGE_STAGING</b> usages. <b>D3D11_USAGE_DEFAULT</b> restricts access almost entirely to the GPU. <b>D3D11_USAGE_STAGING</b> restricts access almost entirely to the CPU and allows only a data transfer (copy) of a resource between the GPU and the CPU. You can perform these copy operations via the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">ID3D11DeviceContext::CopyResource</a> methods. You can also use these copy methods to copy data between two resources of the same usage. You can also use the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">ID3D11DeviceContext::UpdateSubresource</a> method to copy memory directly from a CPU-supplied pointer to any resource, most usefully a resource with <b>D3D11_USAGE_DEFAULT</b>.

<b>D3D11_USAGE_DYNAMIC</b> usage is a special case that optimizes the flow of data from CPU to GPU when the CPU generates that data on-the-fly and sends that data with high frequency. <b>D3D11_USAGE_DYNAMIC</b> is typically used on resources with vertex data and on constant buffers. Use the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-unmap">ID3D11DeviceContext::Unmap</a> methods to write data to these resources. To achieve the highest performance for data consumed serially, like vertex data, use the <b>D3D11_MAP_WRITE_NO_OVERWRITE</b> and <b>D3D11_MAP_WRITE_DISCARD</b> sequence. For more info about this sequence, see <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_map">Common Usage of D3D11_MAP_WRITE_DISCARD with D3D11_MAP_WRITE_NO_OVERWRITE</a>.


<b>D3D11_USAGE_IMMUTABLE</b> usage is another special case that causes the GPU to generate data just once when you create a resource. <b>D3D11_USAGE_IMMUTABLE</b> is well-suited to data such as textures because such data is typically read into memory from some file format. Therefore, when you create a texture with <b>D3D11_USAGE_IMMUTABLE</b>, the GPU directly reads that texture into memory.


Use the following table to choose the usage that best describes how the resource will need to be accessed by the CPU and/or the GPU. Of course, there will be performance tradeoffs.

<table>
<tr>
<th>Resource Usage</th>
<th>Default</th>
<th>Dynamic</th>
<th>Immutable</th>
<th>Staging</th>
</tr>
<tr>
<td>GPU-Read</td>
<td>yes</td>
<td>yes</td>
<td>yes</td>
<td>yes¹</td>
</tr>
<tr>
<td>GPU-Write</td>
<td>yes</td>
<td></td>
<td></td>
<td>yes¹</td>
</tr>
<tr>
<td>CPU-Read</td>
<td></td>
<td></td>
<td></td>
<td>yes¹</td>
</tr>
<tr>
<td>CPU-Write</td>
<td></td>
<td>yes</td>
<td></td>
<td>yes¹</td>
</tr>
</table>
 

1 - GPU read or write of a resource with the <b>D3D11_USAGE_STAGING</b> usage is restricted to copy operations. You use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">ID3D11DeviceContext::CopyResource</a> for these copy operations. Also, because depth-stencil formats and multisample layouts are implementation details of a particular GPU design, the operating system can’t expose these formats and layouts to the CPU in general. Therefore, staging resources can't be a depth-stencil buffer or a multisampled render target.

<div class="alert"><b>Note</b>  You can technically use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">ID3D11DeviceContext::UpdateSubresource</a> to copy to a resource with any usage except <b>D3D11_USAGE_IMMUTABLE</b>. However, we recommend to use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">ID3D11DeviceContext::UpdateSubresource</a> to update only a resource with <b>D3D11_USAGE_DEFAULT</b>. We recommend to use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-unmap">ID3D11DeviceContext::Unmap</a> to update resources with <b>D3D11_USAGE_DYNAMIC</b> because that is the specific purpose of <b>D3D11_USAGE_DYNAMIC</b> resources, and is therefore the most optimized path.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>D3D11_USAGE_DYNAMIC</b> resources consume specific hardware capabilities. Therefore, use them sparingly. The display driver typically allocates memory for <b>D3D11_USAGE_DYNAMIC</b> resources with a caching algorithm that favors CPU writes and hinders CPU reads. Furthermore, the memory behind <b>D3D11_USAGE_DYNAMIC</b> resources might not even be the same for successive calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-map">ID3D11DeviceContext::Map</a>. Therefore, do not expect high performance or even consistent CPU reads from <b>D3D11_USAGE_DYNAMIC</b> resources.</div>
<div> </div>
<div class="alert"><b>Note</b>  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount">ID3D11DeviceContext::CopyStructureCount</a> is a special case of GPU-to-CPU copy. Use <b>ID3D11DeviceContext::CopyStructureCount</b> only with unordered access views (UAVs) of buffers.</div>
<div> </div>
<h3><a id="Bind"></a><a id="bind"></a><a id="BIND"></a>Resource Bind Options</h3>
To maximize performance, not all resource usage options can be used as input or output resources to the pipeline. This table identifies these limitations.

<table>
<tr>
<th>Resource Can Be Bound As</th>
<th>Default</th>
<th>Dynamic</th>
<th>Immutable</th>
<th>Staging</th>
</tr>
<tr>
<td>Input to a Stage</td>
<td>yes²</td>
<td>yes³</td>
<td>yes</td>
<td></td>
</tr>
<tr>
<td>Output from a Stage</td>
<td>yes²</td>
<td></td>
<td></td>
<td></td>
</tr>
</table>
 

<ul>
<li>2 - If bound as an input and an output using different views, each view must use different subresources.</li>
<li>3 - The resource can only be created with a single subresource. The resource cannot be a texture array. The resource cannot be a mipmap chain.</li>
</ul>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
