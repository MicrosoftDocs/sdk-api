---
UID: NS:d3d12.D3D12_VIEWPORT
title: D3D12_VIEWPORT (d3d12.h)
description: Describes the dimensions of a viewport.
helpviewer_keywords: ["D3D12_VIEWPORT","D3D12_VIEWPORT structure","d3d12/D3D12_VIEWPORT","direct3d12.d3d12_viewport"]
old-location: direct3d12\d3d12_viewport.htm
tech.root: direct3d12
ms.assetid: BD23FEF6-8231-45C6-8A6B-F0E42FE88A9F
ms.date: 12/05/2018
ms.keywords: D3D12_VIEWPORT, D3D12_VIEWPORT structure, d3d12/D3D12_VIEWPORT, direct3d12.d3d12_viewport
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
req.typenames: D3D12_VIEWPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_VIEWPORT
 - d3d12/D3D12_VIEWPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_VIEWPORT
---

# D3D12_VIEWPORT structure


## -description

Describes the dimensions of a viewport.

## -struct-fields

### -field TopLeftX

X position of the left hand side of the viewport.

### -field TopLeftY

Y position of the top of the viewport.

### -field Width

Width of the viewport.

### -field Height

Height of the viewport.

### -field MinDepth

Minimum depth of the viewport. Ranges between 0 and 1.

### -field MaxDepth

Maximum depth of the viewport. Ranges between 0 and 1.

## -remarks

Pass an array of these structures to the <i>pViewports</i> parameter  in a call to  <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">ID3D12GraphicsCommandList::RSSetViewports</a> to set viewports for the display.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>