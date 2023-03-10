---
UID: NF:d3d11.ID3D11DeviceContext.ClearState
title: ID3D11DeviceContext::ClearState (d3d11.h)
description: Restore all default settings.
helpviewer_keywords: ["ClearState","ClearState method [Direct3D 11]","ClearState method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","ClearState method","ID3D11DeviceContext.ClearState","ID3D11DeviceContext::ClearState","b3d84ab3-64bc-1c6c-0a7d-5e4409b47dec","d3d11/ID3D11DeviceContext::ClearState","direct3d11.id3d11devicecontext_clearstate"]
old-location: direct3d11\id3d11devicecontext_clearstate.htm
tech.root: direct3d11
ms.assetid: dabf52f5-0f69-4017-863c-9e3ecef4d5dc
ms.date: 12/05/2018
ms.keywords: ClearState, ClearState method [Direct3D 11], ClearState method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearState method, ID3D11DeviceContext.ClearState, ID3D11DeviceContext::ClearState, b3d84ab3-64bc-1c6c-0a7d-5e4409b47dec, d3d11/ID3D11DeviceContext::ClearState, direct3d11.id3d11devicecontext_clearstate
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::ClearState
 - d3d11/ID3D11DeviceContext::ClearState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.ClearState
---

# ID3D11DeviceContext::ClearState


## -description

Restore all default settings.



## -remarks

This method resets any device context to the default settings. This sets all input/output resource slots, shaders, input layouts, predications, scissor rectangles, depth-stencil state, rasterizer state, blend state, sampler state, and viewports to <b>NULL</b>. The primitive topology is set to UNDEFINED.

For a scenario where you would like to clear a list of commands recorded so far, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-finishcommandlist">ID3D11DeviceContext::FinishCommandList</a> and throw away the resulting <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11commandlist">ID3D11CommandList</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
