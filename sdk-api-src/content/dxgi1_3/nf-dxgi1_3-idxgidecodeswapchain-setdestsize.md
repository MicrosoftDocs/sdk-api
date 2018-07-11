---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetDestSize
title: IDXGIDecodeSwapChain::SetDestSize
author: windows-sdk-content
description: Sets the size of the destination surface to use for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_setdestsize.htm
old-project: direct3ddxgi
ms.assetid: BF35FFFE-89C7-4220-9D9F-5BFFE53D3430
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetDestSize method, IDXGIDecodeSwapChain.SetDestSize, IDXGIDecodeSwapChain::SetDestSize, SetDestSize, SetDestSize method [DXGI], SetDestSize method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setdestsize, dxgi1_3/IDXGIDecodeSwapChain::SetDestSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
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
 - IDXGIDecodeSwapChain.SetDestSize
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDecodeSwapChain::SetDestSize


## -description


Sets the size of the destination surface to use for the video processing blit operation.

The destination rectangle is the portion of the output surface that receives the blit for this stream. The destination rectangle is given in pixel coordinates, relative to the output surface.


## -parameters




### -param Width

The width of the destination size, in pixels.


### -param Height

The height of the destination size, in pixels.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

