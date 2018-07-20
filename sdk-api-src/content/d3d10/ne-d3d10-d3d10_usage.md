---
UID: NE:d3d10.D3D10_USAGE
title: D3D10_USAGE
author: windows-sdk-content
description: Identifies expected resource use during rendering. The usage directly reflects whether a resource is accessible by the CPU and/or the GPU.
old-location: direct3d10\d3d10_usage.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_usage.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: D3D10_USAGE, D3D10_USAGE enumeration [Direct3D 10], D3D10_USAGE_DEFAULT, D3D10_USAGE_DYNAMIC, D3D10_USAGE_IMMUTABLE, D3D10_USAGE_STAGING, ce388aa8-48f6-b43d-c978-e00f781ef68c, d3d10/D3D10_USAGE, d3d10/D3D10_USAGE_DEFAULT, d3d10/D3D10_USAGE_DYNAMIC, d3d10/D3D10_USAGE_IMMUTABLE, d3d10/D3D10_USAGE_STAGING, direct3d10.d3d10_usage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d10.h
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
tech.root: 
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_USAGE
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_USAGE enumeration


## -description


Identifies expected resource use during rendering. The usage directly reflects whether a resource is accessible by the CPU and/or the GPU.


## -enum-fields




### -field D3D10_USAGE_DEFAULT

A resource that requires read and write access by the GPU. This is likely to be the most common usage choice.


### -field D3D10_USAGE_IMMUTABLE

A resource that can only be read by the GPU. It cannot be written by the GPU, and cannot be accessed at all by the CPU. This type of resource must be initialized when it is created, since it cannot be changed after creation.


### -field D3D10_USAGE_DYNAMIC

A resource that is accessible by both the GPU and the CPU (write only). A dynamic resource is a good choice for a resource that will be updated by the CPU at least once per frame. To write to a dynamic resource on the CPU, use a <b>Map</b> method. You can write to a dynamic resource on the GPU using <a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">CopyResource</a> or <a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">CopySubresourceRegion</a>.


### -field D3D10_USAGE_STAGING

A resource that supports data transfer (copy) from the GPU to the CPU.


## -remarks



An application identifies the way a resource is intended to be used (its usage) in a resource description. There are several structures for creating resources including: <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a>, <a href="https://msdn.microsoft.com/2535da35-7985-4e50-b840-6a636f871697">D3D10_TEXTURE2D_DESC</a>, <a href="https://msdn.microsoft.com/b2447872-cbef-4cf2-ab7c-2739343ceb64">D3D10_TEXTURE3D_DESC</a>, <a href="https://msdn.microsoft.com/3f98c741-ff4c-4080-bd57-ef35cd6622d6">D3D10_BUFFER_DESC</a>, and <a href="https://msdn.microsoft.com/8325d50e-a8a9-4ee2-87e2-e60fb3699af6">D3DX10_IMAGE_LOAD_INFO</a>.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

In Direct3D 9, you specify the type of memory a resource should be created in at resource creation time (using D3DPOOL). It was an application's job to decide what memory pool would provide the best combination of functionality and performance.

In Direct3D 10, an application no longer specifies what type of memory (the pool) to create a resource in. Instead, you specify the intended usage of the resource, and let the runtime (in concert with the driver and a memory manager) choose the type of memory that will achieve the best performance.

</td>
</tr>
</table>
 

<h3><a id="Restrictions"></a><a id="restrictions"></a><a id="RESTRICTIONS"></a>Resource Usage Restrictions</h3>
Each usage dictates a tradeoff between functionality and performance. In general, resource accessing is accomplished with the following APIs.

<ul>
<li>CPU access is done with <a href="https://msdn.microsoft.com/c863ef55-757d-4c0b-ba59-28d30499cf79">ID3D10Buffer::Map</a>, <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>, <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">ID3D10Texture2D::Map</a>, or <a href="https://msdn.microsoft.com/5cd7a5f0-4a74-4760-a709-d7941025699d">ID3D10Texture3D::Map</a>
</li>
<li>GPU access is done with <a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">CopySubresourceRegion</a>, <a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">CopyResource</a>, or <a href="https://msdn.microsoft.com/eeab4057-4827-4c4b-ae8d-1cbf1f1c9e44">UpdateSubresource</a>.</li>
</ul>
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
<td>yes¹</td>
<td>yes</td>
<td>yes<sup>1, 2</sup></td>
</tr>
<tr>
<td>GPU-Write</td>
<td>yes¹</td>
<td></td>
<td></td>
<td>yes<sup>1, 2</sup></td>
</tr>
<tr>
<td>CPU-Read</td>
<td></td>
<td></td>
<td></td>
<td>yes<sup>1, 2</sup></td>
</tr>
<tr>
<td>CPU-Write</td>
<td></td>
<td>yes</td>
<td></td>
<td>yes<sup>1, 2</sup></td>
</tr>
</table>
 

<ul>
<li>1 - This is restricted to <a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">CopySubresourceRegion</a>, <a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">CopyResource</a>, and <a href="https://msdn.microsoft.com/eeab4057-4827-4c4b-ae8d-1cbf1f1c9e44">UpdateSubresource</a>.</li>
<li>2 - Cannot be a depth-stencil buffer or a multisampled render target.</li>
</ul>
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
<td>yes³</td>
<td>yes⁴</td>
<td>yes</td>
<td></td>
</tr>
<tr>
<td>Output from a Stage</td>
<td>yes³</td>
<td></td>
<td></td>
<td></td>
</tr>
</table>
 

<ul>
<li>3 - If bound as an input and an output using different views, each view must use different <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresources</a>.</li>
<li>4 - The resource can only be created with a single <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a>. The resource cannot be a texture array. The resource cannot be a mipmap chain.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

