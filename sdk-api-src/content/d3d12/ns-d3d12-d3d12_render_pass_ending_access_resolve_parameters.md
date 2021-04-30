---
UID: NS:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
title: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS (d3d12.h)
description: Describes a resource to resolve to at the conclusion of a render pass.
helpviewer_keywords: ["D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS","D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS structure","d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS","direct3d12.d3d12_render_pass_ending_access_resolve_parameters"]
old-location: direct3d12\d3d12_render_pass_ending_access_resolve_parameters.htm
tech.root: direct3d12
ms.assetid: AF081936-CF83-4FFF-BA81-83CEE6F85BFF
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS, D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS structure, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS, direct3d12.d3d12_render_pass_ending_access_resolve_parameters
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
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
 - d3d12/D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
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
 - D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS
---

# D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS structure


## -description

Describes a resource to resolve to at the conclusion of a render pass.

## -struct-fields

### -field pSrcResource

A pointer to an <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>. The source resource.

### -field pDstResource

A pointer to an <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>. The destination resource.

### -field SubresourceCount

A <b>UINT</b>. The number of subresources.

### -field pSubresourceParameters

A pointer to a constant array of <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_subresource_parameters">D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_SUBRESOURCE_PARAMETERS</a>. These subresources can be a subset of the render target's array slices, but you can't target subresources that aren't part of the render target view (RTV) or the depth/stencil view (DSV).

> [!NOTE]
> This pointer is directly referenced by the command list, and the memory for this array must remain alive and intact until [EndRenderPass](nf-d3d12-id3d12graphicscommandlist4-endrenderpass.md) is called.

### -field Format

A <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a>. The data format of the resources.

### -field ResolveMode

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resolve_mode">D3D12_RESOLVE_MODE</a>. The resolve operation.

### -field PreserveResolveSource

A <b>BOOL</b>. <b>TRUE</b> to preserve the resolve source, otherwise <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/direct3d12/rendering">Rendering</a>