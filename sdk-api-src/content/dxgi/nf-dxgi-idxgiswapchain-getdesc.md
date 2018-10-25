---
UID: NF:dxgi.IDXGISwapChain.GetDesc
title: IDXGISwapChain::GetDesc
author: windows-sdk-content
description: Get a description of the swap chain.
old-location: direct3ddxgi\idxgiswapchain_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getdesc.htm
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 545f3a98-5c81-337d-c4f7-cc715e0e123f, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetDesc method, IDXGISwapChain.GetDesc, IDXGISwapChain::GetDesc, direct3ddxgi.idxgiswapchain_getdesc, dxgi/IDXGISwapChain::GetDesc
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
 - IDXGISwapChain.GetDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain::GetDesc


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDesc</b> anymore to get a description of the swap chain. Instead, use <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a>.]

Get a description of the swap chain.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a>*</b>

A pointer to the swap-chain description (see <a href="https://msdn.microsoft.com/en-us/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

