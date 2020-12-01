---
UID: NS:d3d12.D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
title: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC (d3d12.h)
description: Describes a binding (fixed for the duration of the render pass) to a depth stencil view (DSV), as well as its beginning and ending access characteristics.
helpviewer_keywords: ["D3D12_RENDER_PASS_DEPTH_STENCIL_DESC","D3D12_RENDER_PASS_DEPTH_STENCIL_DESC structure","d3d12/D3D12_RENDER_PASS_DEPTH_STENCIL_DESC","direct3d12.d3d12_render_pass_depth_stencil_desc"]
old-location: direct3d12\d3d12_render_pass_depth_stencil_desc.htm
tech.root: direct3d12
ms.assetid: 1C67A6D0-F912-471F-A38C-E3C6A74303EF
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC, D3D12_RENDER_PASS_DEPTH_STENCIL_DESC structure, d3d12/D3D12_RENDER_PASS_DEPTH_STENCIL_DESC, direct3d12.d3d12_render_pass_depth_stencil_desc
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
req.typenames: D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
 - d3d12/D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
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
 - D3D12_RENDER_PASS_DEPTH_STENCIL_DESC
---

# D3D12_RENDER_PASS_DEPTH_STENCIL_DESC structure


## -description

Describes a binding (fixed for the duration of the render pass) to a depth stencil view (DSV), as well as its beginning and ending access characteristics.

## -struct-fields

### -field cpuDescriptor

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a>. The CPU descriptor handle corresponding to the depth stencil view (DSV).

### -field DepthBeginningAccess

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the depth buffer requested at the transition into a render pass.

### -field StencilBeginningAccess

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access">D3D12_RENDER_PASS_BEGINNING_ACCESS</a>. The access to the stencil buffer requested at the transition into a render pass.

### -field DepthEndingAccess

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the depth buffer requested at the transition out of a render pass.

### -field StencilEndingAccess

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access">D3D12_RENDER_PASS_ENDING_ACCESS</a>. The access to the stencil buffer requested at the transition out of a render pass.

## -see-also

<a href="/windows/desktop/direct3d12/rendering">Rendering</a>