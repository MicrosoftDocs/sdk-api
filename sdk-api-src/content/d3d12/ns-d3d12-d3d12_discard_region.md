---
UID: NS:d3d12.D3D12_DISCARD_REGION
title: D3D12_DISCARD_REGION (d3d12.h)
description: Describes details for the discard-resource operation.
helpviewer_keywords: ["D3D12_DISCARD_REGION","D3D12_DISCARD_REGION structure","d3d12/D3D12_DISCARD_REGION","direct3d12.d3d12_discard_region"]
old-location: direct3d12\d3d12_discard_region.htm
tech.root: direct3d12
ms.assetid: 8F0916CB-3389-40BC-8028-BA8CF9BC566B
ms.date: 12/05/2018
ms.keywords: D3D12_DISCARD_REGION, D3D12_DISCARD_REGION structure, d3d12/D3D12_DISCARD_REGION, direct3d12.d3d12_discard_region
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D12_DISCARD_REGION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DISCARD_REGION
 - d3d12/D3D12_DISCARD_REGION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_DISCARD_REGION
---

# D3D12_DISCARD_REGION structure


## -description

Describes details for the discard-resource operation.

## -struct-fields

### -field NumRects

The number of rectangles in the array that the <b>pRects</b> member specifies.

### -field pRects

An array of <b>D3D12_RECT</b> structures for the rectangles in the resource to discard.
            If <b>NULL</b>, <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource">DiscardResource</a> discards the entire resource.

### -field FirstSubresource

Index of the first subresource in the resource to discard.

### -field NumSubresources

The number of subresources in the resource to discard.

## -remarks

This structure is used by the <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource">ID3D12GraphicsCommandList::DiscardResource</a> method.
      

If rectangles are supplied in this structure, the resource must have 2D subresources with all specified subresources the same dimension.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>