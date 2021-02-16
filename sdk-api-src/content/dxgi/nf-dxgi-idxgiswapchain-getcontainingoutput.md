---
UID: NF:dxgi.IDXGISwapChain.GetContainingOutput
title: IDXGISwapChain::GetContainingOutput (dxgi.h)
description: Get the output (the display monitor) that contains the majority of the client area of the target window.
helpviewer_keywords: ["714841de-04d3-ab0c-d428-3902324a14e2","GetContainingOutput","GetContainingOutput method [DXGI]","GetContainingOutput method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetContainingOutput method","IDXGISwapChain.GetContainingOutput","IDXGISwapChain::GetContainingOutput","direct3ddxgi.idxgiswapchain_getcontainingoutput","dxgi/IDXGISwapChain::GetContainingOutput"]
old-location: direct3ddxgi\idxgiswapchain_getcontainingoutput.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getcontainingoutput.htm
ms.date: 12/05/2018
ms.keywords: 714841de-04d3-ab0c-d428-3902324a14e2, GetContainingOutput, GetContainingOutput method [DXGI], GetContainingOutput method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetContainingOutput method, IDXGISwapChain.GetContainingOutput, IDXGISwapChain::GetContainingOutput, direct3ddxgi.idxgiswapchain_getcontainingoutput, dxgi/IDXGISwapChain::GetContainingOutput
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
 - IDXGISwapChain::GetContainingOutput
 - dxgi/IDXGISwapChain::GetContainingOutput
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
 - IDXGISwapChain.GetContainingOutput
---

# IDXGISwapChain::GetContainingOutput


## -description

Get the output (the display monitor) that contains the majority of the client area of the target window.

## -parameters

### -param ppOutput [out]

Type: <b><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>**</b>

A pointer to the output interface (see <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -remarks

If the method succeeds, the output interface will be filled and its reference count incremented. When you are finished with it, be sure to release the interface to avoid a memory leak.

The output is also owned by the adapter on which the swap chain's device was created.

You cannot call <b>GetContainingOutput</b> on a swap chain that you created with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>.

To determine the output corresponding to such a swap chain, you should call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-enumadapters">IDXGIFactory::EnumAdapters</a> and then <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs">IDXGIAdapter::EnumOutputs</a> to enumerate over all of the available outputs. You should then intersect the bounds of your <a href="/uwp/api/windows.ui.core.corewindow.bounds">CoreWindow::Bounds</a> with the desktop coordinates of each output, as reported by <a href="/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1">DXGI_OUTPUT_DESC1::DesktopCoordinates</a> or <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_output_desc">DXGI_OUTPUT_DESC::DesktopCoordinates</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>