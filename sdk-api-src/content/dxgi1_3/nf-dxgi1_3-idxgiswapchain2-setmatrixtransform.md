---
UID: NF:dxgi1_3.IDXGISwapChain2.SetMatrixTransform
title: IDXGISwapChain2::SetMatrixTransform (dxgi1_3.h)
description: Sets the transform matrix that will be applied to a composition swap chain upon the next present.
helpviewer_keywords: ["IDXGISwapChain2 interface [DXGI]","SetMatrixTransform method","IDXGISwapChain2.SetMatrixTransform","IDXGISwapChain2::SetMatrixTransform","SetMatrixTransform","SetMatrixTransform method [DXGI]","SetMatrixTransform method [DXGI]","IDXGISwapChain2 interface","direct3ddxgi.idxgiswapchain2_setmatrixtransform","dxgi1_3/IDXGISwapChain2::SetMatrixTransform"]
old-location: direct3ddxgi\idxgiswapchain2_setmatrixtransform.htm
tech.root: direct3ddxgi
ms.assetid: AAED8A59-3190-49A0-93AA-F5CAF9088877
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain2 interface [DXGI],SetMatrixTransform method, IDXGISwapChain2.SetMatrixTransform, IDXGISwapChain2::SetMatrixTransform, SetMatrixTransform, SetMatrixTransform method [DXGI], SetMatrixTransform method [DXGI],IDXGISwapChain2 interface, direct3ddxgi.idxgiswapchain2_setmatrixtransform, dxgi1_3/IDXGISwapChain2::SetMatrixTransform
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
 - IDXGISwapChain2::SetMatrixTransform
 - dxgi1_3/IDXGISwapChain2::SetMatrixTransform
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
 - IDXGISwapChain2.SetMatrixTransform
---

## -description

Sets the transform matrix that will be applied to a composition swap chain upon the next present. 

Starting with Windows 8.1, Windows Store apps are able to place DirectX swap chain visuals in XAML pages using the <a href="/uwp/api/windows.ui.xaml.controls.swapchainpanel">SwapChainPanel</a> element, which can be placed and sized arbitrarily. This exposes the DirectX swap chain visuals to touch scaling and translation scenarios using touch UI. The <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform">GetMatrixTransform</a> and  <b>SetMatrixTransform</b> methods are used to synchronize scaling of the DirectX swap chain with its associated <b>SwapChainPanel</b> element. Only simple scale/translation elements in the matrix are allowed – the call will fail if the matrix contains skew/rotation elements.

## -parameters

### -param pMatrix

The transform matrix to use for swap chain scaling and translation. This function can only be used with composition swap chains created by <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. Only scale and translation components are allowed in the matrix.

## -returns

<b>SetMatrixTransform</b> returns:
<ul>
<li>S_OK if it successfully retrieves the transform matrix.</li>
<li>E_INVALIDARG if the <i>pMatrix</i> parameter is incorrect, for example, <i>pMatrix</i> is NULL or the matrix represented by <a href="/windows/desktop/api/dxgi1_3/ns-dxgi1_3-dxgi_matrix_3x2_f">DXGI_MATRIX_3X2_F</a> includes components other than scale and translation.</li>
<li>DXGI_ERROR_INVALID_CALL if the method is called on a swap chain that was not created with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">CreateSwapChainForComposition</a>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform">GetMatrixTransform</a>

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>