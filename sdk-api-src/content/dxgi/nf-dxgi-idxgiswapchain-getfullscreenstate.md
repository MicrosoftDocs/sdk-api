---
UID: NF:dxgi.IDXGISwapChain.GetFullscreenState
title: IDXGISwapChain::GetFullscreenState (dxgi.h)
description: Get the state associated with full-screen mode.
helpviewer_keywords: ["GetFullscreenState","GetFullscreenState method [DXGI]","GetFullscreenState method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetFullscreenState method","IDXGISwapChain.GetFullscreenState","IDXGISwapChain::GetFullscreenState","d3b177d7-2b70-fc90-2a07-3046eb5fdf48","direct3ddxgi.idxgiswapchain_getfullscreenstate","dxgi/IDXGISwapChain::GetFullscreenState"]
old-location: direct3ddxgi\idxgiswapchain_getfullscreenstate.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getfullscreenstate.htm
ms.date: 12/05/2018
ms.keywords: GetFullscreenState, GetFullscreenState method [DXGI], GetFullscreenState method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetFullscreenState method, IDXGISwapChain.GetFullscreenState, IDXGISwapChain::GetFullscreenState, d3b177d7-2b70-fc90-2a07-3046eb5fdf48, direct3ddxgi.idxgiswapchain_getfullscreenstate, dxgi/IDXGISwapChain::GetFullscreenState
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain::GetFullscreenState
 - dxgi/IDXGISwapChain::GetFullscreenState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISwapChain.GetFullscreenState
---

# IDXGISwapChain::GetFullscreenState


## -description

Get the state associated with full-screen mode.

## -parameters

### -param pFullscreen [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

A pointer to a boolean whose value is either:


<ul>
<li><b>TRUE</b> if the swap chain is in full-screen mode</li>
<li><b>FALSE</b> if the swap chain is in windowed mode</li>
</ul>

### -param ppTarget [out, optional]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>**</b>

A pointer to the output target (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>) when the mode is full screen; otherwise <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

When the swap chain is in full-screen mode, a pointer to the  target output will be returned and its reference count will be incremented.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>