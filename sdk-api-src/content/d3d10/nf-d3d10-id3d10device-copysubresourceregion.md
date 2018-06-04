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

# ID3D10Device::CopySubresourceRegion


## -description


Copy a region from a source resource to a destination resource.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

A pointer to the destination resource (see <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>).


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Subresource</a> index of the destination.


### -param DstX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The x coordinate of the upper left corner of the destination region.


### -param DstY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The y coordinate of the upper left corner of the destination region.


### -param DstZ [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The z coordinate of the upper left corner of the destination region. For a 1D or 2D subresource, this must be zero.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>*</b>

A pointer to the source resource (see <a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource</a>).


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Subresource</a> index of the source.


### -param pSrcBox [in]

Type: <b>const <a href="https://msdn.microsoft.com/90289ea8-7fa0-47b0-ad3f-43bde1718da1">D3D10_BOX</a>*</b>

A 3D box (see <a href="https://msdn.microsoft.com/90289ea8-7fa0-47b0-ad3f-43bde1718da1">D3D10_BOX</a>) that defines the source subresource that can be copied. If <b>NULL</b>, the entire source subresource is copied. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion</b> doesn't perform a copy operation.


## -returns



Returns nothing




## -remarks



The source box must be within the size of the source resource. The destination location is an absolute value (not a relative value). The destination location can be offset from the source location; however, the size of the region to copy (including the destination location) must fit in the destination resource.

If the resources are buffers, all coordinates are in bytes; if the resources are textures, all coordinates are in texels. 


<a href="https://msdn.microsoft.com/48079797-b5c8-487b-a343-a5623b780350">D3D10CalcSubresource</a> is a helper function for calculating subresource indexes.

<b>CopySubresourceRegion</b> performs the copy on the GPU (similar to a memcpy by the CPU). As a consequence, the source and destination resources must meet the following criteria:

<ul>
<li>Must be different subresources (although they can be from the same resource).</li>
<li>Must be the same <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">type</a>.</li>
<li>Must have compatible <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">formats</a> (the formats must either be identical or be from the same type group). For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to an DXGI_FORMAT_R32G32B32_UINT texture because both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. Beginning with Direct3D 10.1, <b>CopySubresourceRegion</b> can copy between a few format types. For more info, see <a href="d3d10_graphics_programming_guide_resources_block_compression.htm">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">mapped</a>.</li>
</ul>
<b>CopySubresourceRegion</b>  supports only copy; it does not support any stretch, color key, blend, or format conversions. Beginning with Direct3D 10.1, <b>CopySubresourceRegion</b> can reinterpret the resource data between a few format types. For more info, see <a href="d3d10_graphics_programming_guide_resources_block_compression.htm">Format Conversion using Direct3D 10.1</a>.

If your app needs to copy an entire resource, we recommend to use <a href="https://msdn.microsoft.com/3f3f8089-8343-4f83-9208-fd21617b8d19">ID3D10Device::CopyResource</a> instead.

<b>CopySubresourceRegion</b> is an asynchronous call that the runtime can add  to the command-buffer queue. This asynchronous behaviorattempts to remove pipeline stalls that may occur when copying data. See <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">performance considerations</a> for more details.

<table>
<tr>
<td>
Differences between Direct3D 10 and Direct3D 10.1:

Direct3D 10 has the following limitations:

<ul>
<li>You cannot use a depth-stencil resource as a destination.</li>
<li>You cannot use an immutable resource as a destination.</li>
<li>You cannot use a multisampled texture as either a source or a destination</li>
</ul>
Direct3D 10.1 has added support for the following features:

<ul>
<li>You can use a depth-stencil buffer as a source or a destination.</li>
<li>You can use multisampled resources as  source and destination only if both source and destination have identical multisampled count and quality. If source and destination differ in multisampled count and quality or if the source is multisampled and the destination is not multisampled (or vice versa), the call to <b>ID3D10Device::CopySubresourceRegion</b> fails.</li>
<li>You can copy between uncompressed and compressed resources. During copy, the format conversions that are specified in  <a href="https://msdn.microsoft.com/add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5">Format Conversion using Direct3D 10.1</a> are supported automatically. The uncompressed resource must be at least prestructured, and typed. You must also account for the difference between the virtual and the physical size of the mipmaps levels.</li>
</ul>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you use <b>CopySubresourceRegion</b> with a depth-stencil buffer or a multisampled resource, you must copy the whole subresource. You must also pass 0 to the <i>DstX</i>, <i>DstY</i>, and <i>DstZ</i> parameters and <b>NULL</b> to the <i>pSrcBox</i> parameter. In addition, source and destination resources, which are represented by the <i>pSrcResource</i> and <i>pDstResource</i> parameters respectively, must have identical sample count values.</div>
<div> </div>
<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following code snippet copies a box (located at (120,100),(200,220)) from a source texture into a reqion (130,120),(210,240) in a destination texture.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
D3D10_BOX sourceRegion;
sourceRegion.left = 120;
sourceRegion.right = 200;
sourceRegion.top = 100;
sourceRegion.bottom = 220;
sourceRegion.front = 0;
sourceRegion.back = 1;

pd3dDevice-&gt;CopySubresourceRegion( pDestTexture, 0, 130, 120, 0, pSourceTexture, 0, &amp;sourceRegion );
</pre>
</td>
</tr>
</table></span></div>
Notice that, for a 2D texture, front and back are always set to 0 and 1 respectively.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device</a>



<a href="https://msdn.microsoft.com/709c6f33-e1dc-4609-8ddd-9dc502628ec5">ID3D10Resource Interface</a>
 

 

