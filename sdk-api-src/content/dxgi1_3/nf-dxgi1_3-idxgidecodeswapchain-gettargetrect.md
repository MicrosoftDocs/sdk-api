---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetTargetRect
title: IDXGIDecodeSwapChain::GetTargetRect
author: windows-sdk-content
description: Gets the rectangle that defines the target region for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_gettargetrect.htm
old-project: direct3ddxgi
ms.assetid: 1B42CE33-7130-433F-940F-B45D3152BB33
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetTargetRect, GetTargetRect method [DXGI], GetTargetRect method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetTargetRect method, IDXGIDecodeSwapChain.GetTargetRect, IDXGIDecodeSwapChain::GetTargetRect, direct3ddxgi.idxgidecodeswapchain_gettargetrect, dxgi1_3/IDXGIDecodeSwapChain::GetTargetRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDecodeSwapChain.GetTargetRect
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDecodeSwapChain::GetTargetRect


## -description


Gets the rectangle that defines the target region for the video processing blit operation.


## -parameters




### -param pRect [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure 
        that receives the target region for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

