---
UID: NF:d3d11.ID3D11DeviceContext.CopyResource
title: ID3D11DeviceContext::CopyResource (d3d11.h)
description: Copy the entire contents of the source resource to the destination resource using the GPU. (ID3D11DeviceContext.CopyResource)
helpviewer_keywords: ["CopyResource","CopyResource method [Direct3D 11]","CopyResource method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","CopyResource method","ID3D11DeviceContext.CopyResource","ID3D11DeviceContext::CopyResource","b389573e-412e-6a72-6e59-396d4bd62341","d3d11/ID3D11DeviceContext::CopyResource","direct3d11.id3d11devicecontext_copyresource"]
old-location: direct3d11\id3d11devicecontext_copyresource.htm
tech.root: direct3d11
ms.assetid: 54c1c08a-792c-463d-8237-9f7947d15396
ms.date: 12/05/2018
ms.keywords: CopyResource, CopyResource method [Direct3D 11], CopyResource method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],CopyResource method, ID3D11DeviceContext.CopyResource, ID3D11DeviceContext::CopyResource, b389573e-412e-6a72-6e59-396d4bd62341, d3d11/ID3D11DeviceContext::CopyResource, direct3d11.id3d11devicecontext_copyresource
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
 - ID3D11DeviceContext::CopyResource
 - d3d11/ID3D11DeviceContext::CopyResource
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
 - ID3D11DeviceContext.CopyResource
---

# ID3D11DeviceContext::CopyResource


## -description

Copy the entire contents of the source resource to the destination resource using the GPU.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface that represents the destination resource.

### -param pSrcResource [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a> interface that represents the source resource.

## -remarks

This method is unusual in that it causes the GPU to perform the copy operation (similar to a memcpy by the CPU). As a result, it has a few restrictions designed for improving performance. For instance, the source and destination resources:

<ul>
<li>Must be different resources.</li>
<li>Must be the same type.</li>
<li>Must have identical dimensions (including width, height, depth, and size as appropriate).</li>
<li>Must have compatible <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI formats</a>, which means the formats must be identical or at least from the same type group. For example, a DXGI_FORMAT_R32G32B32_FLOAT texture can be copied to a DXGI_FORMAT_R32G32B32_UINT texture since both of these formats are in the DXGI_FORMAT_R32G32B32_TYPELESS group. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">CopyResource</a> can copy between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.</li>
<li>Can't be currently mapped.</li>
</ul>
<b>CopyResource</b> only supports copy; it doesn't support any stretch, color key, or blend. <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">CopyResource</a> can reinterpret the resource data between a few format types. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-block-compression">Format Conversion using Direct3D 10.1</a>.

You can't use an <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_usage">Immutable</a> resource as a destination. You can use a   <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag">depth-stencil</a> resource as either a source or a destination provided that the feature level is D3D_FEATURE_LEVEL_10_1 or greater. For feature levels 9_x, resources created with the D3D11_BIND_DEPTH_STENCIL flag can only be used as a source for <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-copyresource">CopyResource</a>.  Resources created with multisampling capability (see <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc">DXGI_SAMPLE_DESC</a>) can be used as source and destination only if both source and destination have identical multisampled count and quality. If source and destination differ in multisampled count and quality or if one is multisampled and the other is not multisampled, the call to <b>ID3D11DeviceContext::CopyResource</b> fails. Use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ID3D11DeviceContext::ResolveSubresource</a> to resolve a multisampled resource to a resource that is not multisampled.

The method is an asynchronous call, which may be added to the command-buffer queue. This attempts to remove pipeline stalls that may occur when copying data. For more info, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping">performance considerations</a>.

We recommend to use <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">ID3D11DeviceContext::CopySubresourceRegion</a> instead if you only need to copy a portion of the data in a resource.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>
