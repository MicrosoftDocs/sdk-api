---
UID: NF:dxgi.IDXGISwapChain.ResizeTarget
title: IDXGISwapChain::ResizeTarget (dxgi.h)
author: windows-sdk-content
description: Resizes the output target.
old-location: direct3ddxgi\idxgiswapchain_resizetarget.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_resizetarget.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain interface [DXGI],ResizeTarget method, IDXGISwapChain.ResizeTarget, IDXGISwapChain::ResizeTarget, ResizeTarget, ResizeTarget method [DXGI], ResizeTarget method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_resizetarget, dxgi/IDXGISwapChain::ResizeTarget, f136baf7-17fc-2a80-f25e-e0fc612bcad7
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IDXGISwapChain::ResizeTarget


## -description


Resizes the output target.


## -parameters




### -param pNewTargetParameters [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb173064(v=VS.85).aspx">DXGI_MODE_DESC</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb173064(v=VS.85).aspx">DXGI_MODE_DESC</a> structure that describes the mode, which specifies the new width, height, format, and refresh rate of the target. 
        If the format is <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT_UNKNOWN</a>, <b>ResizeTarget</b> uses the existing format. We only recommend that you use <b>DXGI_FORMAT_UNKNOWN</b> when the swap chain is in full-screen 
        mode as this method is not thread safe.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns a code that indicates success or failure. <b>DXGI_STATUS_MODE_CHANGE_IN_PROGRESS</b> is returned if a full-screen/windowed mode transition is occurring 
      when this API is called. See <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> for additional DXGI error codes.




## -remarks



<b>ResizeTarget</b> resizes the target window when the swap chain is in windowed mode, and changes the display mode on the target output when the swap 
      chain is in full-screen mode. Therefore, apps can call <b>ResizeTarget</b> to resize the target window (rather than a Microsoft Win32API such as <a href="https://msdn.microsoft.com/en-us/library/ms633545(v=VS.85).aspx">SetWindowPos</a>) 
      without knowledge of the swap chain display mode.

If a Windows Store app calls <b>ResizeTarget</b>, it fails with <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

You cannot call <b>ResizeTarget</b> on a swap chain that you created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.

Apps must still call <a href="https://msdn.microsoft.com/en-us/library/Bb174577(v=VS.85).aspx">IDXGISwapChain::ResizeBuffers</a> after they call <b>ResizeTarget</b> because only <b>ResizeBuffers</b> can change the back buffers. But, if those apps have implemented window resize processing to call <b>ResizeBuffers</b>, they don't need to explicitly call <b>ResizeBuffers</b> after they call <b>ResizeTarget</b> because the window resize processing will achieve what the app requires.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

