---
UID: NS:d3d12.D3D12_RENDER_PASS_ENDING_ACCESS
title: D3D12_RENDER_PASS_ENDING_ACCESS (d3d12.h)
description: Describes the access to resource(s) that is requested by an application at the transition out of a render pass.
helpviewer_keywords: ["D3D12_RENDER_PASS_ENDING_ACCESS","D3D12_RENDER_PASS_ENDING_ACCESS structure","d3d12/D3D12_RENDER_PASS_ENDING_ACCESS","direct3d12.d3d12_render_pass_ending_access"]
old-location: direct3d12\d3d12_render_pass_ending_access.htm
tech.root: direct3d12
ms.assetid: 1BEE91E3-3462-4A13-88CE-31806BC451EA
ms.date: 12/05/2018
ms.keywords: D3D12_RENDER_PASS_ENDING_ACCESS, D3D12_RENDER_PASS_ENDING_ACCESS structure, d3d12/D3D12_RENDER_PASS_ENDING_ACCESS, direct3d12.d3d12_render_pass_ending_access
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
req.typenames: D3D12_RENDER_PASS_ENDING_ACCESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RENDER_PASS_ENDING_ACCESS
 - d3d12/D3D12_RENDER_PASS_ENDING_ACCESS
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
 - D3D12_RENDER_PASS_ENDING_ACCESS
---

# D3D12_RENDER_PASS_ENDING_ACCESS structure


## -description

Describes the access to resource(s) that is requested by an application at the transition out of a render pass.

## -struct-fields

### -field Type

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type">D3D12_RENDER_PASS_ENDING_ACCESS_TYPE</a>. The type of access being requested.

### -field Resolve

A <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access_resolve_parameters">D3D12_RENDER_PASS_ENDING_ACCESS_RESOLVE_PARAMETERS</a>. Appropriate when  <b>Type</b> is <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type">D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_RESOLVE</a>. Description of the resource to resolve to.

## -see-also

<a href="/windows/desktop/direct3d12/rendering">Rendering</a>