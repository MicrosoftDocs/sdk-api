---
UID: NF:dxgi.IDXGISwapChain.GetFullscreenState
title: IDXGISwapChain::GetFullscreenState
author: windows-sdk-content
description: Get the state associated with full-screen mode.
old-location: direct3ddxgi\idxgiswapchain_getfullscreenstate.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getfullscreenstate.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFullscreenState, GetFullscreenState method [DXGI], GetFullscreenState method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetFullscreenState method, IDXGISwapChain.GetFullscreenState, IDXGISwapChain::GetFullscreenState, d3b177d7-2b70-fc90-2a07-3046eb5fdf48, direct3ddxgi.idxgiswapchain_getfullscreenstate, dxgi/IDXGISwapChain::GetFullscreenState
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDXGISwapChain.GetFullscreenState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain::GetFullscreenState


## -description


Get the state associated with full-screen mode.


## -parameters




### -param pFullscreen [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

A pointer to a boolean whose value is either:


<ul>
<li><b>TRUE</b> if the swap chain is in full-screen mode</li>
<li><b>FALSE</b> if the swap chain is in windowed mode</li>
</ul>

### -param ppTarget [out, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>**</b>

A pointer to the output target (see <a href="https://msdn.microsoft.com/en-us/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>) when the mode is full screen; otherwise <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -remarks



When the swap chain is in full-screen mode, a pointer to the  target output will be returned and its reference count will be incremented.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

