---
UID: NF:dxgi1_2.IDXGISwapChain1.GetFullscreenDesc
title: IDXGISwapChain1::GetFullscreenDesc (dxgi1_2.h)
description: Gets a description of a full-screen swap chain.
helpviewer_keywords: ["GetFullscreenDesc","GetFullscreenDesc method [DXGI]","GetFullscreenDesc method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetFullscreenDesc method","IDXGISwapChain1.GetFullscreenDesc","IDXGISwapChain1::GetFullscreenDesc","direct3ddxgi.idxgiswapchain1_getfullscreendesc","dxgi1_2/IDXGISwapChain1::GetFullscreenDesc"]
old-location: direct3ddxgi\idxgiswapchain1_getfullscreendesc.htm
tech.root: direct3ddxgi
ms.assetid: 6056239A-B3CA-4C70-9081-499B0AAEFBEF
ms.date: 12/05/2018
ms.keywords: GetFullscreenDesc, GetFullscreenDesc method [DXGI], GetFullscreenDesc method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetFullscreenDesc method, IDXGISwapChain1.GetFullscreenDesc, IDXGISwapChain1::GetFullscreenDesc, direct3ddxgi.idxgiswapchain1_getfullscreendesc, dxgi1_2/IDXGISwapChain1::GetFullscreenDesc
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
 - IDXGISwapChain1::GetFullscreenDesc
 - dxgi1_2/IDXGISwapChain1::GetFullscreenDesc
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
 - IDXGISwapChain1.GetFullscreenDesc
---

# IDXGISwapChain1::GetFullscreenDesc


## -description

Gets a description of a full-screen swap chain.

## -parameters

### -param pDesc [out]

A pointer to a <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_fullscreen_desc">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a>  structure that describes the full-screen swap chain.

## -returns

<b>GetFullscreenDesc</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the description of the full-screen swap chain.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a>  for non-<a href="/windows/desktop/WinProg/windows-data-types">HWND</a> swap chains or if <i>pDesc</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic. </li>
</ul>

## -remarks

The semantics of <b>GetFullscreenDesc</b> are identical to that of the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getdesc">IDXGISwapchain::GetDesc</a> method for <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>-based swap chains.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>