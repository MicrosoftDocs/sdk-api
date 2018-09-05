---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetSourceRect
title: IDXGIDecodeSwapChain::SetSourceRect
author: windows-sdk-content
description: Sets the rectangle that defines the source region for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_setsourcerect.htm
old-project: direct3ddxgi
ms.assetid: E614D9C2-9AAC-4ADC-9B7B-99C47975DA07
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetSourceRect method, IDXGIDecodeSwapChain.SetSourceRect, IDXGIDecodeSwapChain::SetSourceRect, SetSourceRect, SetSourceRect method [DXGI], SetSourceRect method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setsourcerect, dxgi1_3/IDXGIDecodeSwapChain::SetSourceRect
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
 - IDXGIDecodeSwapChain.SetSourceRect
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDecodeSwapChain::SetSourceRect


## -description


Sets the rectangle that defines the source region for the video processing blit operation.

The source rectangle is the portion of the input surface that is blitted to the destination surface. The source rectangle is given in pixel coordinates, relative to the input surface.


## -parameters




### -param pRect

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure 
        that contains the source region to set for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

