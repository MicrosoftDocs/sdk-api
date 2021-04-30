---
UID: NF:dxgi1_3.IDXGISwapChain2.GetMatrixTransform
title: IDXGISwapChain2::GetMatrixTransform (dxgi1_3.h)
description: Gets the transform matrix that will be applied to a composition swap chain upon the next present.
helpviewer_keywords: ["GetMatrixTransform","GetMatrixTransform method [DXGI]","GetMatrixTransform method [DXGI]","IDXGISwapChain2 interface","IDXGISwapChain2 interface [DXGI]","GetMatrixTransform method","IDXGISwapChain2.GetMatrixTransform","IDXGISwapChain2::GetMatrixTransform","direct3ddxgi.idxgiswapchain2_getmatrixtransform","dxgi1_3/IDXGISwapChain2::GetMatrixTransform"]
old-location: direct3ddxgi\idxgiswapchain2_getmatrixtransform.htm
tech.root: direct3ddxgi
ms.assetid: 90302283-BB0A-44A9-8CD2-591571EF74ED
ms.date: 12/05/2018
ms.keywords: GetMatrixTransform, GetMatrixTransform method [DXGI], GetMatrixTransform method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetMatrixTransform method, IDXGISwapChain2.GetMatrixTransform, IDXGISwapChain2::GetMatrixTransform, direct3ddxgi.idxgiswapchain2_getmatrixtransform, dxgi1_3/IDXGISwapChain2::GetMatrixTransform
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain2::GetMatrixTransform
 - dxgi1_3/IDXGISwapChain2::GetMatrixTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2.GetMatrixTransform
---

## -description

Gets the transform matrix that will be applied to a composition swap chain upon the next present. 

Starting with Windows 8.1, Windows Store apps are able to place DirectX swap chain visuals in XAML pages using the <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a> element, which can be placed and sized arbitrarily. This exposes the DirectX swap chain visuals to touch scaling and translation scenarios using touch UI. The <b>GetMatrixTransform</b> and  <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform">SetMatrixTransform</a> methods are used to synchronize scaling of the DirectX swap chain with its associated <b>SwapChainPanel</b> element. Only simple scale/translation elements in the matrix are allowed – the call will fail if the matrix contains skew/rotation elements.

## -parameters

### -param pMatrix

[out]

The transform matrix currently used for swap chain scaling and translation.

## -returns

<b>GetMatrixTransform</b> returns:
<ul>
<li>S_OK if it successfully retrieves the transform matrix.</li>
<li>DXGI_ERROR_INVALID_CALL if the method is called on a swap chain that was not created with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">CreateSwapChainForComposition</a>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform">SetMatrixTransform</a>