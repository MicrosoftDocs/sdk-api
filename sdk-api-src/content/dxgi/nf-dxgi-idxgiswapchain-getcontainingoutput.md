---
UID: NF:dxgi.IDXGISwapChain.GetContainingOutput
title: IDXGISwapChain::GetContainingOutput
author: windows-sdk-content
description: Get the output (the display monitor) that contains the majority of the client area of the target window.
old-location: direct3ddxgi\idxgiswapchain_getcontainingoutput.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getcontainingoutput.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 714841de-04d3-ab0c-d428-3902324a14e2, GetContainingOutput, GetContainingOutput method [DXGI], GetContainingOutput method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetContainingOutput method, IDXGISwapChain.GetContainingOutput, IDXGISwapChain::GetContainingOutput, direct3ddxgi.idxgiswapchain_getcontainingoutput, dxgi/IDXGISwapChain::GetContainingOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
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
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::GetContainingOutput


## -description


Get the output (the display monitor) that contains the majority of the client area of the target window.


## -parameters




### -param ppOutput [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>**</b>

A pointer to the output interface (see <a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



If the method succeeds, the output interface will be filled and its reference count incremented. When you are finished with it, be sure to release the interface to avoid a memory leak.

The output is also owned by the adapter on which the swap chain's device was created.

You cannot call <b>GetContainingOutput</b> on a swap chain that you created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.

To determine the output corresponding to such a swap chain, you should call <a href="https://msdn.microsoft.com/library/Bb174538(v=VS.85).aspx">IDXGIFactory::EnumAdapters</a> and then <a href="https://msdn.microsoft.com/library/Bb174525(v=VS.85).aspx">IDXGIAdapter::EnumOutputs</a> to enumerate over all of the available outputs. You should then intersect the bounds of your <a href="https://msdn.microsoft.com/e189b0c0-4a8d-418c-8509-f94130f24226">CoreWindow::Bounds</a> with the desktop coordinates of each output, as reported by <a href="https://msdn.microsoft.com/5215EF2C-9511-4B21-B574-3447FA5896F7">DXGI_OUTPUT_DESC1::DesktopCoordinates</a> or <a href="https://msdn.microsoft.com/library/Bb173068(v=VS.85).aspx">DXGI_OUTPUT_DESC::DesktopCoordinates</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

