---
UID: NF:d3d10.ID3D10Device.CopySubresourceRegion
title: ID3D10Device::CopySubresourceRegion (d3d10.h)
description: Copy a region from a source resource to a destination resource. (ID3D10Device.CopySubresourceRegion)
helpviewer_keywords: ["6ed5c759-9864-ef56-3e1a-e3f8ff730dff","CopySubresourceRegion","CopySubresourceRegion method [Direct3D 10]","CopySubresourceRegion method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CopySubresourceRegion method","ID3D10Device.CopySubresourceRegion","ID3D10Device::CopySubresourceRegion","d3d10/ID3D10Device::CopySubresourceRegion","direct3d10.id3d10device_copysubresourceregion"]
old-location: direct3d10\id3d10device_copysubresourceregion.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_copysubresourceregion.htm
ms.date: 12/05/2018
ms.keywords: 6ed5c759-9864-ef56-3e1a-e3f8ff730dff, CopySubresourceRegion, CopySubresourceRegion method [Direct3D 10], CopySubresourceRegion method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CopySubresourceRegion method, ID3D10Device.CopySubresourceRegion, ID3D10Device::CopySubresourceRegion, d3d10/ID3D10Device::CopySubresourceRegion, direct3d10.id3d10device_copysubresourceregion
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::CopySubresourceRegion
 - d3d10/ID3D10Device::CopySubresourceRegion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.CopySubresourceRegion
---

# ID3D10Device::CopySubresourceRegion


## -description

Copy a region from a source resource to a destination resource.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

A pointer to the destination resource (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>).

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Subresource</a> index of the destination.

### -param DstX [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The x coordinate of the upper left corner of the destination region.

### -param DstY [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The y coordinate of the upper left corner of the destination region.

### -param DstZ [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The z coordinate of the upper left corner of the destination region. For a 1D or 2D subresource, this must be zero.

### -param pSrcResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

A pointer to the source resource (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>).

### -param SrcSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Subresource</a> index of the source.

### -param pSrcBox [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_box">D3D10_BOX</a>*</b>

A 3D box (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_box">D3D10_BOX</a>) that defines the source subresource that can be copied. If <b>NULL</b>, the entire source subresource is copied. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion</b> doesn't perform a copy operation.

## -remarks

The source box must be within the size of the source resource. The destination location is an absolute value (not a relative value). The destination location can be offset from the source location; however, the size of the region to copy (including the destination location) must fit in the destination resource.

If the resources are buffers, all coordinates are in bytes; if the resources are textures, all coordinates are in texels. 


<a href="/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> is a helper function for calculating subresource indexes.

<b>CopySubresourceRegion</b> performs the copy on the GPU (similar to a memcpy by the CPU). As a consequence, the source and destination resources must meet the following criteria:

<ul>
<li>Must be different subresources (although they can be from the same resource).</li>
<li>Must be the same <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">type</a>.</li>
<li>Must have compatible <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">formats</a> (the formats must either be identical or be from the same type group). For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture because both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. Beginning with Direct3D 10.1, <b>CopySubresourceRegion</b> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">mapped</a>.</li>
</ul>
<b>CopySubresourceRegion</b>  supports only copy; it does not support any stretch, color key, blend, or format conversions. Beginning with Direct3D 10.1, <b>CopySubresourceRegion</b> can reinterpret the resource data between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.

If your app needs to copy an entire resource, we recommend to use <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">ID3D10Device::CopyResource</a> instead.

<b>CopySubresourceRegion</b> is an asynchronous call that the runtime can add  to the command-buffer queue. This asynchronous behaviorattempts to remove pipeline stalls that may occur when copying data. See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">performance considerations</a> for more details.

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
<li>You can copy between uncompressed and compressed resources. During copy, the format conversions that are specified in  <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a> are supported automatically. The uncompressed resource must be at least prestructured, and typed. You must also account for the difference between the virtual and the physical size of the mipmaps levels.</li>
</ul>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  If you use <b>CopySubresourceRegion</b> with a depth-stencil buffer or a multisampled resource, you must copy the whole subresource. You must also pass 0 to the <i>DstX</i>, <i>DstY</i>, and <i>DstZ</i> parameters and <b>NULL</b> to the <i>pSrcBox</i> parameter. In addition, source and destination resources, which are represented by the <i>pSrcResource</i> and <i>pDstResource</i> parameters respectively, must have identical sample count values.</div>
<div> </div>
<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following code snippet copies a box (located at (120,100),(200,220)) from a source texture into a region (130,120),(210,240) in a destination texture.


```

D3D10_BOX sourceRegion;
sourceRegion.left = 120;
sourceRegion.right = 200;
sourceRegion.top = 100;
sourceRegion.bottom = 220;
sourceRegion.front = 0;
sourceRegion.back = 1;

pd3dDevice->CopySubresourceRegion( pDestTexture, 0, 130, 120, 0, pSourceTexture, 0, &sourceRegion );

```


Notice that, for a 2D texture, front and back are always set to 0 and 1 respectively.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a>
