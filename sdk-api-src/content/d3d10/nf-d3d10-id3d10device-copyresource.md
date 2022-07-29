---
UID: NF:d3d10.ID3D10Device.CopyResource
title: ID3D10Device::CopyResource (d3d10.h)
description: Copy the entire contents of the source resource to the destination resource using the GPU. (ID3D10Device.CopyResource)
helpviewer_keywords: ["7cc09321-049c-23b4-3867-f1b76d332515","CopyResource","CopyResource method [Direct3D 10]","CopyResource method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","CopyResource method","ID3D10Device.CopyResource","ID3D10Device::CopyResource","d3d10/ID3D10Device::CopyResource","direct3d10.id3d10device_copyresource"]
old-location: direct3d10\id3d10device_copyresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_copyresource.htm
ms.date: 12/05/2018
ms.keywords: 7cc09321-049c-23b4-3867-f1b76d332515, CopyResource, CopyResource method [Direct3D 10], CopyResource method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],CopyResource method, ID3D10Device.CopyResource, ID3D10Device::CopyResource, d3d10/ID3D10Device::CopyResource, direct3d10.id3d10device_copyresource
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
 - ID3D10Device::CopyResource
 - d3d10/ID3D10Device::CopyResource
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
 - ID3D10Device.CopyResource
---

# ID3D10Device::CopyResource


## -description

Copy the entire contents of the source resource to the destination resource using the GPU.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

A pointer to the destination resource (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>).

### -param pSrcResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

A pointer to the source resource (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>).

## -remarks

This method is unusual in that it causes the GPU to perform the copy operation (similar to a memcpy by the CPU). As a result, it has a few restrictions designed for improving performance. For instance, the source and destination resources:

<ul>
<li>Must be different resources.</li>
<li>Must be the same <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">type</a>.</li>
<li>Must have identical dimensions (including width, height, depth, and size as appropriate).</li>
<li>Must have compatible <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">formats</a>, which means the formats must be identical or at least from the same type group. For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. Beginning with Direct3D 10.1, <b>CopyResource</b> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.</li>
<li>May not be currently <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">mapped</a>.</li>
</ul>
<b>CopyResource</b>  supports only copy; it does not support any stretch, color key, blend, or format conversions. Beginning with Direct3D 10.1, <b>CopyResource</b> can reinterpret the resource data between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.


<a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">Immutable</a>, and <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag">depth-stencil</a> resources cannot be used as a destination.  Resources created with <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">multisampling capability</a> cannot be used as either a source or destination.

The method is an asynchronous call which may be added to the command-buffer queue. This attempts to remove pipeline stalls that may occur when copying data. See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">performance considerations</a> for more details.

An application that only needs to copy a portion of the data in a resource should use <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copysubresourceregion">ID3D10Device::CopySubresourceRegion</a> instead.

<table>
<tr>
<td>
Differences between Direct3D 10 and Direct3D 10.1:

Direct3D 10.1 enables depth-stencil resources to be used as either a source or destination. Direct3D 10.1 enables multisampled resources to be used as source and destination only if both source and destination have identical multisampled count and quality. If source and destination differ in multisampled count and quality or one of them is multisampled and the other is not multisampled, the call to <b>ID3D10Device::CopyResource</b> fails.

It is possible to copy between prestructured+typed resources and block-compressed textures. See <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>



<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource Interface</a>
