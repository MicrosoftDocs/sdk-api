---
UID: NF:dxgi.IDXGISwapChain.GetLastPresentCount
title: IDXGISwapChain::GetLastPresentCount (dxgi.h)
description: Gets the number of times that IDXGISwapChain::Present or IDXGISwapChain1::Present1 has been called.
helpviewer_keywords: ["GetLastPresentCount","GetLastPresentCount method [DXGI]","GetLastPresentCount method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetLastPresentCount method","IDXGISwapChain.GetLastPresentCount","IDXGISwapChain::GetLastPresentCount","direct3ddxgi.idxgiswapchain_getlastpresentcount","dxgi/IDXGISwapChain::GetLastPresentCount","f6292a4d-50a6-18b3-5edc-a581c15fa784"]
old-location: direct3ddxgi\idxgiswapchain_getlastpresentcount.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getlastpresentcount.htm
ms.date: 12/05/2018
ms.keywords: GetLastPresentCount, GetLastPresentCount method [DXGI], GetLastPresentCount method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetLastPresentCount method, IDXGISwapChain.GetLastPresentCount, IDXGISwapChain::GetLastPresentCount, direct3ddxgi.idxgiswapchain_getlastpresentcount, dxgi/IDXGISwapChain::GetLastPresentCount, f6292a4d-50a6-18b3-5edc-a581c15fa784
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
 - IDXGISwapChain::GetLastPresentCount
 - dxgi/IDXGISwapChain::GetLastPresentCount
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
 - IDXGISwapChain.GetLastPresentCount
---

# IDXGISwapChain::GetLastPresentCount


## -description

Gets the number of times  that <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> has been called.

## -parameters

### -param pLastPresentCount [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that receives the number of calls.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

For info about presentation statistics for a frame, see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_frame_statistics">DXGI_FRAME_STATISTICS</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>