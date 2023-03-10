---
UID: NF:d3d12.ID3D12GraphicsCommandList1.ResolveSubresourceRegion
title: ID3D12GraphicsCommandList1::ResolveSubresourceRegion (d3d12.h)
description: Copy a region of a multisampled or compressed resource into a non-multisampled or non-compressed resource.
helpviewer_keywords: ["ID3D12GraphicsCommandList1 interface","ResolveSubresourceRegion method","ID3D12GraphicsCommandList1.ResolveSubresourceRegion","ID3D12GraphicsCommandList1::ResolveSubresourceRegion","ResolveSubresourceRegion","ResolveSubresourceRegion method","ResolveSubresourceRegion method","ID3D12GraphicsCommandList1 interface","d3d12/ID3D12GraphicsCommandList1::ResolveSubresourceRegion","direct3d12.id3d12graphicscommandlist1_resolvesubresourceregion"]
old-location: direct3d12\id3d12graphicscommandlist1_resolvesubresourceregion.htm
tech.root: direct3d12
ms.assetid: 8CF3809C-0EC7-4FBB-AEEF-E74FCD9B836D
ms.date: 08/10/2022
ms.keywords: ID3D12GraphicsCommandList1 interface,ResolveSubresourceRegion method, ID3D12GraphicsCommandList1.ResolveSubresourceRegion, ID3D12GraphicsCommandList1::ResolveSubresourceRegion, ResolveSubresourceRegion, ResolveSubresourceRegion method, ResolveSubresourceRegion method,ID3D12GraphicsCommandList1 interface, d3d12/ID3D12GraphicsCommandList1::ResolveSubresourceRegion, direct3d12.id3d12graphicscommandlist1_resolvesubresourceregion
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
 - ID3D12GraphicsCommandList1::ResolveSubresourceRegion
 - d3d12/ID3D12GraphicsCommandList1::ResolveSubresourceRegion
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
 - ID3D12GraphicsCommandList1.ResolveSubresourceRegion
---

# ID3D12GraphicsCommandList1::ResolveSubresourceRegion


## -description

Copy a region of a multisampled or compressed resource into a non-multisampled or non-compressed resource.

## -parameters

### -param pDstResource [in]

Type: <b>ID3D12Resource*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Destination resource. Must be created with the <b>D3D11_USAGE_DEFAULT</b> flag and must be single-sampled unless its to be resolved from a compressed resource (<b>D3D12_RESOLVE_MODE_DECOMPRESS</b>); in this case it must have the same sample count as the compressed source.

### -param DstSubresource [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

A zero-based index that identifies the destination subresource. Use <a href="/windows/desktop/direct3d12/d3d12calcsubresource">D3D12CalcSubresource</a> to calculate the subresource index if the parent resource is complex.

### -param DstX [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

The X coordinate of the left-most edge of the destination region. The width of the destination region is the same as the width of the source rect.

### -param DstY [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

The Y coordinate of the top-most edge of the destination region. The height of the destination region is the same as the height of the source rect.

### -param pSrcResource [in]

Type: <b>ID3D12Resource*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Source resource. Must be multisampled or compressed.

### -param SrcSubresource [in]

Type: <b>UINT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

A zero-based index that identifies the source subresource.

### -param pSrcRect [in, optional]

Type: <b>D3D12_RECT*</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_opt_</code>

Specifies the rectangular region of the source resource to be resolved. Passing NULL for <i>pSrcRect</i> specifies that the entire subresource is to be resolved.

### -param Format [in]

Type: <b>DXGI_FORMAT</b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

A DXGI_FORMAT that specifies how the source and destination resource formats are consolidated.

### -param ResolveMode [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resolve_mode">D3D12_RESOLVE_MODE</a></b>

<a href="/visualstudio/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Specifies the operation used to resolve the source samples.

When using the <b>D3D12_RESOLVE_MODE_DECOMPRESS</b> operation, the sample count can be larger than 1 as long as the source and destination have the same sample count, and source and destination may specify the same resource as long as the source rect aligns with the destination X and Y coordinates, in which case decompression occurs in place.

When using the <b>D3D12_RESOLVE_MODE_MIN</b>, <b>D3D12_RESOLVE_MODE_MAX</b>, or <b>D3D12_RESOLVE_MODE_AVERAGE</b> operation, the destination must have a sample count of 1.

## -remarks

ResolveSubresourceRegion operates like <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource">ResolveSubresource</a> but allows for only part of a resource to be resolved and for source samples to be resolved in several ways. Partial resolves can be useful in multi-adapter scenarios; for example, when the rendered area has been partitioned across adapters, each adapter might only need to resolve the portion of a subresource that corresponds to its assigned partition.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>