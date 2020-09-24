---
UID: NF:d3d10sdklayers.ID3D10Debug.SetSwapChain
title: ID3D10Debug::SetSwapChain (d3d10sdklayers.h)
description: Set a swap chain that the runtime will use for automatically calling Present.
helpviewer_keywords: ["ID3D10Debug interface [Direct3D 10]","SetSwapChain method","ID3D10Debug.SetSwapChain","ID3D10Debug::SetSwapChain","SetSwapChain","SetSwapChain method [Direct3D 10]","SetSwapChain method [Direct3D 10]","ID3D10Debug interface","b58e521c-faea-98fb-6fb5-01fb1131f1a6","d3d10sdklayers/ID3D10Debug::SetSwapChain","direct3d10.id3d10debug_setswapchain"]
old-location: direct3d10\id3d10debug_setswapchain.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setswapchain.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Debug interface [Direct3D 10],SetSwapChain method, ID3D10Debug.SetSwapChain, ID3D10Debug::SetSwapChain, SetSwapChain, SetSwapChain method [Direct3D 10], SetSwapChain method [Direct3D 10],ID3D10Debug interface, b58e521c-faea-98fb-6fb5-01fb1131f1a6, d3d10sdklayers/ID3D10Debug::SetSwapChain, direct3d10.id3d10debug_setswapchain
req.header: d3d10sdklayers.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Debug::SetSwapChain
 - d3d10sdklayers/ID3D10Debug::SetSwapChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetSwapChain
---

# ID3D10Debug::SetSwapChain


## -description

Set a swap chain that the runtime will use for automatically calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>.

## -parameters

### -param pSwapChain [in]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>*</b>

Swap chain that the runtime will use for automatically calling <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>; must have been created with the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain">DXGI_SWAP_EFFECT_SEQUENTIAL</a> swap-effect flag.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The swap chain set by this method will only be used if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask">feature mask</a>.

## -see-also

<a href="/windows/desktop/api/d3d10sdklayers/nn-d3d10sdklayers-id3d10debug">ID3D10Debug Interface</a>