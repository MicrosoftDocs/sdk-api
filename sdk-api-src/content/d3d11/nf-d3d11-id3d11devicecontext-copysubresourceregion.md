---
UID: NF:d3d11.ID3D11DeviceContext.CopySubresourceRegion
title: ID3D11DeviceContext::CopySubresourceRegion (d3d11.h)
description: Copy a region from a source resource to a destination resource. (ID3D11DeviceContext.CopySubresourceRegion)
helpviewer_keywords: ["4fcc18c3-ca99-b51e-9162-bb8b4121db03","CopySubresourceRegion","CopySubresourceRegion method [Direct3D 11]","CopySubresourceRegion method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CopySubresourceRegion method","ID3D11DeviceContext.CopySubresourceRegion","ID3D11DeviceContext::CopySubresourceRegion","d3d11/ID3D11DeviceContext::CopySubresourceRegion","direct3d11.id3d11devicecontext_copysubresourceregion"]
old-location: direct3d11\id3d11devicecontext_copysubresourceregion.htm
tech.root: direct3d11
ms.assetid: aed89483-9870-445d-96e3-a9cee764f0ad
ms.date: 12/05/2018
ms.keywords: 4fcc18c3-ca99-b51e-9162-bb8b4121db03, CopySubresourceRegion, CopySubresourceRegion method [Direct3D 11], CopySubresourceRegion method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopySubresourceRegion method, ID3D11DeviceContext.CopySubresourceRegion, ID3D11DeviceContext::CopySubresourceRegion, d3d11/ID3D11DeviceContext::CopySubresourceRegion, direct3d11.id3d11devicecontext_copysubresourceregion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::CopySubresourceRegion
 - d3d11/ID3D11DeviceContext::CopySubresourceRegion
dev_langs:
 - c++
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
---

# ID3D11DeviceContext::CopySubresourceRegion


## -description

Copy a region from a source resource to a destination resource.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the destination resource (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>).

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Destination subresource index.

### -param DstX [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The x-coordinate of the upper left corner of the destination region.

### -param DstY [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The y-coordinate of the upper left corner of the destination region. For a 1D subresource, this must be zero.

### -param DstZ [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The z-coordinate of the upper left corner of the destination region. For a 1D or 2D subresource, this must be zero.

### -param pSrcResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the source resource (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>).

### -param SrcSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Source subresource index.

### -param pSrcBox [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>*</b>

A pointer to a 3D box (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_box">D3D11_BOX</a>) that defines the source subresource that can be copied. If <b>NULL</b>, the entire source subresource is copied. The box must fit within the source resource.

An empty box results in a no-op. A box is empty if the top value is greater than or equal to the bottom value, or the left value is greater than or equal to the right value, or the front value is greater than or equal to the back value. When the box is empty, <b>CopySubresourceRegion</b> doesn't perform a copy operation.

## -remarks

The source box must be within the size of the source resource. The destination offsets, (x, y, and z), allow the source box to be offset when writing into the destination resource; however, the dimensions of the source box and the offsets must be within the size of the resource. If you try and copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of <b>CopySubresourceRegion</b> is undefined. If you created a device that supports the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a>, the debug output reports an error on this invalid <b>CopySubresourceRegion</b> call. Invalid parameters to <b>CopySubresourceRegion</b> cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.

If the resources are buffers, all coordinates are in bytes; if the resources are textures, all coordinates are in texels. <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11calcsubresource">D3D11CalcSubresource</a> is a helper function for calculating subresource indexes.

<b>CopySubresourceRegion</b> performs the copy on the GPU (similar to a memcpy by the CPU). As a consequence, the source and destination resources:

<ul>
<li>Must be different subresources (although they can be from the same resource).</li>
<li>Must be the same type.</li>
<li>Must have compatible DXGI formats (identical or from the same type group). For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <b>CopySubresourceRegion</b> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently mapped.</li>
</ul>

**CopySubresourceRegion** only supports copy; it doesn't support any stretch, color key, or blend. **CopySubresourceRegion** can reinterpret the resource data between a few format types. For more info, see [Format conversion using Direct3D 10.1](/windows/win32/direct3d10/d3d10-graphics-programming-guide-resources-block-compression#format-conversion-using-direct3d-101).

If your app needs to copy an entire resource, we recommend to use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">ID3D11DeviceContext::CopyResource</a> instead.
        

<b>CopySubresourceRegion</b> is an asynchronous call, which may be added to the command-buffer queue, this attempts to remove pipeline stalls that may occur when copying data. For more information about pipeline stalls, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">performance considerations</a>.

<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> If you use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">ID3D11DeviceContext::UpdateSubresource</a> or <b>CopySubresourceRegion</b> to copy from a staging resource to a default resource, you can corrupt the destination contents. This occurs if you pass a <b>NULL</b> source box and if the source resource has different dimensions from those of the destination resource or if you use destination offsets, (x, y, and z). In this situation, always pass a source box that is the full size of the source resource.</div>
<div> </div>
<div class="alert"><b>Note</b>  <b>Applies only to feature level 9_x hardware</b> You can't use <b>CopySubresourceRegion</b> to copy mipmapped volume textures. </div>
<div> </div>
<div class="alert"><b>Note</b>  <b>Applies only to feature levels 9_x</b> Subresources created with the D3D11_BIND_DEPTH_STENCIL flag can only be used as a source for <b>CopySubresourceRegion</b>.</div>
<div> </div>
<div class="alert"><b>Note</b>  If you use <b>CopySubresourceRegion</b> with a depth-stencil buffer or a multisampled resource, you must copy the whole subresource. In this situation, you must pass 0 to the <i>DstX</i>, <i>DstY</i>, and <i>DstZ</i> parameters and <b>NULL</b> to the <i>pSrcBox</i> parameter. In addition, source and destination resources, which are represented by the <i>pSrcResource</i> and <i>pDstResource</i> parameters, should have identical sample count values.</div>
<div> </div>
<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following code snippet copies a box (located at (120,100),(200,220)) from a source texture into a region (10,20),(90,140) in a destination texture.
          


```
D3D11_BOX sourceRegion;
sourceRegion.left = 120;
sourceRegion.right = 200;
sourceRegion.top = 100;
sourceRegion.bottom = 220;
sourceRegion.front = 0;
sourceRegion.back = 1;

pd3dDeviceContext->CopySubresourceRegion( pDestTexture, 0, 10, 20, 0, pSourceTexture, 0, &sourceRegion );

```


Notice, that for a 2D texture, front and back are set to 0 and 1 respectively.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>
