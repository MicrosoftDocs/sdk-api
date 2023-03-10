---
UID: NS:d3d12.D3D12_BUFFER_RTV
title: D3D12_BUFFER_RTV (d3d12.h)
description: Describes the elements in a buffer resource to use in a render-target view.
helpviewer_keywords: ["D3D12_BUFFER_RTV","D3D12_BUFFER_RTV structure","d3d12/D3D12_BUFFER_RTV","direct3d12.d3d12_buffer_rtv"]
old-location: direct3d12\d3d12_buffer_rtv.htm
tech.root: direct3d12
ms.assetid: B4BDA7DE-6FB1-4806-9207-42EA0BFC69AE
ms.date: 12/05/2018
ms.keywords: D3D12_BUFFER_RTV, D3D12_BUFFER_RTV structure, d3d12/D3D12_BUFFER_RTV, direct3d12.d3d12_buffer_rtv
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
req.typenames: D3D12_BUFFER_RTV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_BUFFER_RTV
 - d3d12/D3D12_BUFFER_RTV
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
 - D3D12_BUFFER_RTV
---

# D3D12_BUFFER_RTV structure


## -description

Describes the elements in a buffer resource to use in a render-target view.

## -struct-fields

### -field FirstElement

Number of elements between the beginning of the buffer and the first element to access.

### -field NumElements

The total number of elements in the view.

## -remarks

Use this structure with a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc">D3D12_RENDER_TARGET_VIEW_DESC</a> structure to view the resource as a buffer.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>