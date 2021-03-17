---
UID: NS:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS
title: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS (d3d12.h)
description: Describes the subresources involved in resolving at the conclusion of a render pass.
helpviewer_keywords: ["D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS","D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS structure","d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS","direct3d12.d3d12_render_pass_ending_access_resolve_subresource_parameters"]
old-location: direct3d12\d3d12_render_pass_ending_access_resolve_subresource_parameters.htm
tech.root: direct3d12
ms.assetid: 1A063782-2EE9-4D79-BF5D-0C160048E95E
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS, D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS structure, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS, direct3d12.d3d12_render_pass_ending_access_resolve_subresource_parameters
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
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS
 - d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS
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
 - D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS
---

# D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS structure


## -description

Describes the subresources involved in resolving at the conclusion of a render pass.

## -struct-fields

### -field SrcSubresource

A <b>UINT</b>. The source subresource.

### -field DstSubresource

A <b>UINT</b>. The destination subresource.

### -field DstX

A <b>UINT</b>. The x coordinate within the destination subresource.

### -field DstY

A <b>UINT</b>. The y coordinate within the destination subresource.

### -field SrcRect

A <a href="/windows/desktop/direct3d12/d3d12-rect">D3D12_RECT</a>. The rectangle within the source subresource.

## -see-also

<a href="/windows/desktop/direct3d12/rendering">Rendering</a>