---
UID: NF:d3d12.ID3D12GraphicsCommandList.ResolveSubresource
title: ID3D12GraphicsCommandList::ResolveSubresource (d3d12.h)
description: Copy a multi-sampled resource into a non-multi-sampled resource.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","ResolveSubresource method","ID3D12GraphicsCommandList.ResolveSubresource","ID3D12GraphicsCommandList::ResolveSubresource","ResolveSubresource","ResolveSubresource method","ResolveSubresource method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::ResolveSubresource","direct3d12.id3d12graphicscommandlist_resolvesubresource"]
old-location: direct3d12\id3d12graphicscommandlist_resolvesubresource.htm
tech.root: direct3d12
ms.assetid: F1D4BAD1-B08E-47D0-9D2B-41873D6B4456
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,ResolveSubresource method, ID3D12GraphicsCommandList.ResolveSubresource, ID3D12GraphicsCommandList::ResolveSubresource, ResolveSubresource, ResolveSubresource method, ResolveSubresource method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::ResolveSubresource, direct3d12.id3d12graphicscommandlist_resolvesubresource
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::ResolveSubresource
 - d3d12/ID3D12GraphicsCommandList::ResolveSubresource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.ResolveSubresource
---

## -description

Copy a multi-sampled resource into a non-multi-sampled resource.

## -parameters

### -param pDstResource

Type: [in] <b>ID3D12Resource*</b>

Destination resource. Must be a created on a <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_type">D3D12_HEAP_TYPE_DEFAULT</a> heap and be single-sampled. See <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>.

### -param DstSubresource

Type: [in] <b>UINT</b>

A zero-based index, that identifies the destination subresource. Use <a href="/windows/win32/direct3d12/d3d12calcsubresource">D3D12CalcSubresource</a> to calculate the subresource index if the parent resource is complex.

### -param pSrcResource

Type: [in] <b>ID3D12Resource*</b>

Source resource. Must be multisampled.

### -param SrcSubresource

Type: [in] <b>UINT</b>

The source subresource of the source resource.

### -param Format

Type: [in] <b>DXGI_FORMAT</b>

A <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> that indicates how the multisampled resource will be resolved to a single-sampled resource. See remarks.

## -remarks

<h3><a id="Debug_layer"></a><a id="debug_layer"></a><a id="DEBUG_LAYER"></a>Debug layer</h3>
The debug layer will issue an error if the subresources referenced by the source view is not in the  <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_RESOLVE_SOURCE</a> state.

The debug layer will issue an error if the destination buffer is not in the  <a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states">D3D12_RESOURCE_STATE_RESOLVE_DEST</a> state.

The source and destination resources must be the same resource type and have the same dimensions. In addition, they must have compatible formats. There are three scenarios for this:

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
<td>Both the source and destination must have the same typeless format (i.e. both must have DXGI_FORMAT_R32_TYPELESS), and the Format parameter must specify a format that is compatible with the source and destination (i.e. if both are DXGI_FORMAT_R32_TYPELESS then DXGI_FORMAT_R32_FLOAT could be specified in the Format parameter).
              For example, given the DXGI_FORMAT_R16G16B16A16_TYPELESS format:
              

<ul>
<li>The source (or dest) format could be DXGI_FORMAT_R16G16B16A16_UNORM</li>
<li>The dest (or source) format could be DXGI_FORMAT_R16G16B16A16_FLOAT</li>
</ul>
</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>

<a href="/windows/win32/direct3d12/subresources">Subresources</a>

