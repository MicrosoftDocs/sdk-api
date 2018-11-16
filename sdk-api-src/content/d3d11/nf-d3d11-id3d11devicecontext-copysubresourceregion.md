---
UID: NF:d3d11.ID3D11DeviceContext.CopySubresourceRegion
title: ID3D11DeviceContext::CopySubresourceRegion
author: windows-sdk-content
description: Copy a region from a source resource to a destination resource.
old-location: direct3d11\id3d11devicecontext_copysubresourceregion.htm
tech.root: direct3d11
ms.assetid: aed89483-9870-445d-96e3-a9cee764f0ad
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 4fcc18c3-ca99-b51e-9162-bb8b4121db03, CopySubresourceRegion, CopySubresourceRegion method [Direct3D 11], CopySubresourceRegion method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopySubresourceRegion method, ID3D11DeviceContext.CopySubresourceRegion, ID3D11DeviceContext::CopySubresourceRegion, d3d11/ID3D11DeviceContext::CopySubresourceRegion, direct3d11.id3d11devicecontext_copysubresourceregion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.CopySubresourceRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.CopySubresourceRegion
: 
---

# ID3D11DeviceContext::CopySubresourceRegion


## -description


Copy a region from a source resource to a destination resource.


## -parameters




### -param pDstResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the destination resource (see <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>).


### -param DstSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Destination subresource index.


### -param DstX [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The x-coordinate of the upper left corner of the destination region.


### -param DstY [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The y-coordinate of the upper left corner of the destination region. For a 1D subresource, this must be zero.


### -param DstZ [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The z-coordinate of the upper left corner of the destination region. For a 1D or 2D subresource, this must be zero.


### -param pSrcResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

A pointer to the source resource (see <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>).


### -param SrcSubresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Source subresource index.


### -param pSrcBox [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>*</b>

A pointer to a 3D box (see <a href="https://msdn.microsoft.com/0cc98805-a36e-41aa-a24f-51fbcf5070df">D3D11_BOX</a>) that defines the source subresource that can be copied. If <b>NULL</b>, the entire source subresource is copied. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion</b> doesn't perform a copy operation.


## -returns



Returns nothing




## -remarks



The source box must be within the size of the source resource. The destination offsets, (x, y, and z), allow the source box to be offset when writing into the destination resource; however, the dimensions of the source box and the offsets must be within the size of the resource. If you try and copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of <b>CopySubresourceRegion</b> is undefined. If you created a device that supports the <a href="overviews_direct3d_11_devices_layers.htm">debug layer</a>, the debug output reports an error on this invalid <b>CopySubresourceRegion</b> call. Invalid parameters to <b>CopySubresourceRegion</b> cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.

If the resources are buffers, all coordinates are in bytes; if the resources are textures, all coordinates are in texels. <a href="https://msdn.microsoft.com/643a21f7-3c2e-4d62-9236-051f51d31241">D3D11CalcSubresource</a> is a helper function for calculating subresource indexes.

<b>CopySubresourceRegion</b> performs the copy on the GPU (similar to a memcpy by the CPU). As a consequence, the source and destination resources:

<ul>
<li>Must be different subresources (although they can be from the same resource).</li>
<li>Must be the same type.</li>
<li>Must have compatible DXGI formats (identical or from the same type group). For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to an DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <b>CopySubresourceRegion</b> can copy between a few format types. For more info, see <a href="https://msdn.microsoft.com/add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently mapped.</li>
</ul>
<b>CopySubresourceRegion</b> only supports copy; it does not support any stretch, color key, or blend. <b>CopySubresourceRegion</b> can reinterpret the resource data between a few format types. For more info, see <a href="https://msdn.microsoft.com/add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5">Format Conversion using Direct3D 10.1</a>.

If your app needs to copy an entire resource, we recommend to use <a href="https://msdn.microsoft.com/54c1c08a-792c-463d-8237-9f7947d15396">ID3D11DeviceContext::CopyResource</a> instead.
        

<b>CopySubresourceRegion</b> is an asynchronous call, which may be added to the command-buffer queue, this attempts to remove pipeline stalls that may occur when copying data. For more information about pipeline stalls, see <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">performance considerations</a>.

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">ID3D11DeviceContext::UpdateSubresource</a> or <b>CopySubresourceRegion</b> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> You can't use <b>CopySubresourceRegion</b> to copy mipmapped volume textures. </div>
<div> </div>
<div class="alert"><b>Note</b>  <b>Applies only to feature levels 9_x</b> Subresources created with the D3D11_BIND_DEPTH_STENCIL flag can only be used as a source for <b>CopySubresourceRegion</b>.</div>
<div> </div>
<div class="alert"><b>Note</b>  If you use <b>CopySubresourceRegion</b> with a depth-stencil buffer or a multisampled resource, you must copy the whole subresource. In this situation, you must pass 0 to the <i>DstX</i>, <i>DstY</i>, and <i>DstZ</i> parameters and <b>NULL</b> to the <i>pSrcBox</i> parameter. In addition, source and destination resources, which are represented by the <i>pSrcResource</i> and <i>pDstResource</i> parameters, should have identical sample count values.</div>
<div> </div>
<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following code snippet copies a box (located at (120,100),(200,220)) from a source texture into a reqion (10,20),(90,140) in a destination texture.
          

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>D3D11_BOX sourceRegion;
sourceRegion.left = 120;
sourceRegion.right = 200;
sourceRegion.top = 100;
sourceRegion.bottom = 220;
sourceRegion.front = 0;
sourceRegion.back = 1;

pd3dDeviceContext-&gt;CopySubresourceRegion( pDestTexture, 0, 10, 20, 0, pSourceTexture, 0, &amp;sourceRegion );
</pre>
</td>
</tr>
</table></span></div>
Notice, that for a 2D texture, front and back are set to 0 and 1 respectively.
          




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>



<a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>
 

 

