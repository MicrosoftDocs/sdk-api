---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D10Device::CopyResource


## -description


Copy the entire contents of the source resource to the destination resource using the GPU. 


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

A pointer to the destination resource (see <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>).


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

A pointer to the source resource (see <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>).


## -returns



Returns nothing




## -remarks



This method is unusual in that it causes the GPU to perform the copy operation (similar to a memcpy by the CPU). As a result, it has a few restrictions designed for improving performance. For instance, the source and destination resources:

<ul>
<li>Must be different resources.</li>
<li>Must be the same <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">type</a>.</li>
<li>Must have identical dimensions (including width, height, depth, and size as appropriate).</li>
<li>Must have compatible <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">formats</a>, which means the formats must be identical or at least from the same type group. For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to an DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. Beginning with Direct3D 10.1, <b>CopyResource</b> can copy between a few format types. For more info, see <a href="d3d10_graphics_programming_guide_resources_block_compression.htm">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">mapped</a>.</li>
</ul>
<b>CopyResource</b>  supports only copy; it does not support any stretch, color key, blend, or format conversions. Beginning with Direct3D 10.1, <b>CopyResource</b> can reinterpret the resource data between a few format types. For more info, see <a href="d3d10_graphics_programming_guide_resources_block_compression.htm">Format Conversion using Direct3D 10.1</a>.


<a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">Immutable</a>, and <a href="https://msdn.microsoft.com/3bbefc3b-ad05-499b-bbec-f370bf08a7f4">depth-stencil</a> resources cannot be used as a destination.  Resources created with <a href="https://msdn.microsoft.com/a8071d3c-dc78-43fe-84f6-421418e16b02">multisampling capability</a> cannot be used as either a source or destination.

The method is an asynchronous call which may be added to the command-buffer queue. This attempts to remove pipeline stalls that may occur when copying data. See <a href="d3d10_graphics_programming_guide_resources_mapping.htm">performance considerations</a> for more details.

An application that only needs to copy a portion of the data in a resource should use <a href="https://msdn.microsoft.com/78803e46-9945-45d4-a7cc-41f527831251">ID3D10Device::CopySubresourceRegion</a> instead.

<table>
<tr>
<td>
Differences between Direct3D 10 and Direct3D 10.1:

Direct3D 10.1 enables depth-stencil resources to be used as either a source or destination. Direct3D 10.1 enables multisampled resources to be used as source and destination only if both source and destination have identical multisampled count and quality. If source and destination differ in multisampled count and quality or one of them is multisampled and the other is not multisampled, the call to <b>ID3D10Device::CopyResource</b> fails.

It is possible to copy between prestructured+typed resources and block-compressed textures. See <a href="d3d10_graphics_programming_guide_resources_block_compression.htm">Format Conversion using Direct3D 10.1</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>



<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource Interface</a>
 

 

