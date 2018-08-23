---
UID: NF:dxgi.IDXGISwapChain.ResizeTarget
title: IDXGISwapChain::ResizeTarget
author: windows-sdk-content
description: Resizes the output target.
old-location: direct3ddxgi\idxgiswapchain_resizetarget.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_resizetarget.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IDXGISwapChain interface [DXGI],ResizeTarget method, IDXGISwapChain.ResizeTarget, IDXGISwapChain::ResizeTarget, ResizeTarget, ResizeTarget method [DXGI], ResizeTarget method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_resizetarget, dxgi/IDXGISwapChain::ResizeTarget, f136baf7-17fc-2a80-f25e-e0fc612bcad7
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi.h
req.include-header: 
req.redist: 
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
 - IDXGISwapChain.ResizeTarget
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::ResizeTarget


## -description


Resizes the output target.


## -parameters




### -param pNewTargetParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a> structure that describes the mode, which specifies the new width, height, format, and refresh rate of the target. 
        If the format is <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_UNKNOWN</a>, <b>ResizeTarget</b> uses the existing format. We only recommend that you use <b>DXGI_FORMAT_UNKNOWN</b> when the swap chain is in full-screen 
        mode as this method is not thread safe.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns a code that indicates success or failure. <b>DXGI_STATUS_MODE_CHANGE_IN_PROGRESS</b> is returned if a full-screen/windowed mode transition is occurring 
      when this API is called. See <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> for additional DXGI error codes.




## -remarks



<b>ResizeTarget</b> resizes the target window when the swap chain is in windowed mode, and changes the display mode on the target output when the swap 
      chain is in full-screen mode. Therefore, apps can call <b>ResizeTarget</b> to resize the target window (rather than a Microsoft Win32API such as <a href="https://msdn.microsoft.com/e0a28590-0fed-4ffa-adcd-84b60df316b5">SetWindowPos</a>) 
      without knowledge of the swap chain display mode.

If a Windows Store app calls <b>ResizeTarget</b>, it fails with <a href="dxgi_error.htm">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

You cannot call <b>ResizeTarget</b> on a swap chain that you created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.

Apps must still call <a href="https://msdn.microsoft.com/c70aaad0-e742-4ff1-9d25-80d171f3f9de">IDXGISwapChain::ResizeBuffers</a> after they call <b>ResizeTarget</b> because only <b>ResizeBuffers</b> can change the back buffers. But, if those apps have implemented window resize processing to call <b>ResizeBuffers</b>, they don't need to explicitly call <b>ResizeBuffers</b> after they call <b>ResizeTarget</b> because the window resize processing will achieve what the app requires.




## -see-also




<a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>
 

 

