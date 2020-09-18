---
UID: NF:dxgi1_2.IDXGISwapChain1.GetBackgroundColor
title: IDXGISwapChain1::GetBackgroundColor (dxgi1_2.h)
description: Retrieves the background color of the swap chain.
helpviewer_keywords: ["GetBackgroundColor","GetBackgroundColor method [DXGI]","GetBackgroundColor method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetBackgroundColor method","IDXGISwapChain1.GetBackgroundColor","IDXGISwapChain1::GetBackgroundColor","direct3ddxgi.idxgiswapchain1_getbackgroundcolor","dxgi1_2/IDXGISwapChain1::GetBackgroundColor"]
old-location: direct3ddxgi\idxgiswapchain1_getbackgroundcolor.htm
tech.root: direct3ddxgi
ms.assetid: AF10BAF1-5C49-45E7-B776-3EB606C02E10
ms.date: 12/05/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [DXGI], GetBackgroundColor method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetBackgroundColor method, IDXGISwapChain1.GetBackgroundColor, IDXGISwapChain1::GetBackgroundColor, direct3ddxgi.idxgiswapchain1_getbackgroundcolor, dxgi1_2/IDXGISwapChain1::GetBackgroundColor
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain1::GetBackgroundColor
 - dxgi1_2/IDXGISwapChain1::GetBackgroundColor
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
 - IDXGISwapChain1.GetBackgroundColor
---

# IDXGISwapChain1::GetBackgroundColor


## -description

Retrieves the background color of the swap chain.

## -parameters

### -param pColor [out]

A pointer to a <a href="/windows/desktop/direct3ddxgi/dxgi-rgba">DXGI_RGBA</a> structure that receives the background color of the swap chain.

## -returns

<b>GetBackgroundColor</b> returns:
        <ul>
<li>S_OK if it successfully retrieves the background color.</li>
<li>
<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if the <i>pColor</i> parameter is invalid, for example, <i>pColor</i> is NULL.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -remarks

<div class="alert"><b>Note</b>  The background color that <b>GetBackgroundColor</b> retrieves does not indicate what the screen currently displays. The background color indicates what the screen will display with your next call to the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> method. The default value of the background color is black with full opacity: 0,0,0,1.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor">IDXGISwapChain1::SetBackgroundColor</a>