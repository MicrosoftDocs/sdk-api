---
UID: NF:d3d10.ID3D10Device.ResolveSubresource
title: ID3D10Device::ResolveSubresource (d3d10.h)
description: Copy a multisampled resource into a non-multisampled resource. This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","ResolveSubresource method","ID3D10Device.ResolveSubresource","ID3D10Device::ResolveSubresource","ResolveSubresource","ResolveSubresource method [Direct3D 10]","ResolveSubresource method [Direct3D 10]","ID3D10Device interface","ba86f6c0-1c03-0ae4-a93b-f0475c4a5a37","d3d10/ID3D10Device::ResolveSubresource","direct3d10.id3d10device_resolvesubresource"]
old-location: direct3d10\id3d10device_resolvesubresource.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_resolvesubresource.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],ResolveSubresource method, ID3D10Device.ResolveSubresource, ID3D10Device::ResolveSubresource, ResolveSubresource, ResolveSubresource method [Direct3D 10], ResolveSubresource method [Direct3D 10],ID3D10Device interface, ba86f6c0-1c03-0ae4-a93b-f0475c4a5a37, d3d10/ID3D10Device::ResolveSubresource, direct3d10.id3d10device_resolvesubresource
req.header: d3d10.h
req.include-header: D3d10core
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::ResolveSubresource
 - d3d10/ID3D10Device::ResolveSubresource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d10.h
api_name:
 - ID3D10Device.ResolveSubresource
---

# ID3D10Device::ResolveSubresource


## -description

Copy a multisampled resource into a non-multisampled resource. This API is most useful when re-using the resulting rendertarget of one render pass as an input to a second render pass.

## -parameters

### -param pDstResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

Destination resource. Must be a created with the <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_usage">D3D10_USAGE_DEFAULT</a> flag and be single-sampled. See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>.

### -param DstSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index, that identifies the destination subresource. See <a href="/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.

### -param pSrcResource [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>*</b>

Source resource. Must be multisampled.

### -param SrcSubresource [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The source subresource of the source resource.

### -param Format [in]

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>


<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> that indicates how the multisampled resource will be resolved to a single-sampled resource. See remarks.

## -remarks

Both the source and destination resources must be the same <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">resource type</a> and have the same dimensions.

The source and destination must have compatible formats. There are three scenarios for this:

<table>
<tr>
<th>Scenario</th>
<th>Requirements</th>
</tr>
<tr>
<td>Source and destination are prestructured and typed</td>
<td>Both the source and destination must have identical formats and that format must be specified in the Format parameter.</td>
</tr>
<tr>
<td>One resource is prestructured and typed and the other is prestructured and typeless</td>
<td>The typed resource must have a format that is compatible with the typeless resource (i.e. the typed resource is DXGI_FORMAT_R32_FLOAT and the typeless resource is DXGI_FORMAT_R32_TYPELESS). The format of the typed resource must be specified in the Format parameter.</td>
</tr>
<tr>
<td>Source and destination are prestructured and typeless</td>
<td>Both the source and destination must have the same typeless format (i.e. both must have DXGI_FORMAT_R32_TYPELESS), and the Format parameter must specify a format that is compatible with the source and destination (i.e. if both are DXGI_FORMAT_R32_TYPELESS then DXGI_FORMAT_R32_FLOAT or DXGI_FORMAT_R32_UINT could be specified in the Format parameter).</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>