---
UID: NF:dxgi1_2.IDXGISwapChain1.GetHwnd
title: IDXGISwapChain1::GetHwnd (dxgi1_2.h)
description: Retrieves the underlying HWND for this swap-chain object.
helpviewer_keywords: ["GetHwnd","GetHwnd method [DXGI]","GetHwnd method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetHwnd method","IDXGISwapChain1.GetHwnd","IDXGISwapChain1::GetHwnd","direct3ddxgi.idxgiswapchain1_gethwnd","dxgi1_2/IDXGISwapChain1::GetHwnd"]
old-location: direct3ddxgi\idxgiswapchain1_gethwnd.htm
tech.root: direct3ddxgi
ms.assetid: C1690710-FA63-4841-B3E2-68200E0B7B23
ms.date: 12/05/2018
ms.keywords: GetHwnd, GetHwnd method [DXGI], GetHwnd method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetHwnd method, IDXGISwapChain1.GetHwnd, IDXGISwapChain1::GetHwnd, direct3ddxgi.idxgiswapchain1_gethwnd, dxgi1_2/IDXGISwapChain1::GetHwnd
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain1::GetHwnd
 - dxgi1_2/IDXGISwapChain1::GetHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.GetHwnd
---

# IDXGISwapChain1::GetHwnd


## -description

Retrieves the underlying <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> for this swap-chain object.

## -parameters

### -param pHwnd [out]

A pointer to a variable that receives the <a href="/windows/desktop/WinProg/windows-data-types">HWND</a> for the swap-chain object.

## -returns

Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

If <i>pHwnd</i> receives <b>NULL</b> (that is, the swap chain is not <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>-based), <b>GetHwnd</b> returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>.

## -remarks

Applications call the  <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a> method to create a swap chain that is associated with an <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>