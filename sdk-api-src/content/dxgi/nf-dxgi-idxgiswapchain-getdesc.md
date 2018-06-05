---
UID: NF:dxgi.IDXGISwapChain.GetDesc
title: IDXGISwapChain::GetDesc
author: windows-sdk-content
description: Get a description of the swap chain.
old-location: direct3ddxgi\idxgiswapchain_getdesc.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getdesc.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: 545f3a98-5c81-337d-c4f7-cc715e0e123f, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetDesc method, IDXGISwapChain.GetDesc, IDXGISwapChain::GetDesc, direct3ddxgi.idxgiswapchain_getdesc, dxgi/IDXGISwapChain::GetDesc
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGISwapChain.GetDesc
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::GetDesc


## -description


<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDesc</b> anymore to get a description of the swap chain. Instead, use <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a>.]

Get a description of the swap chain.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>*</b>

A pointer to the swap-chain description (see <a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>
 

 

