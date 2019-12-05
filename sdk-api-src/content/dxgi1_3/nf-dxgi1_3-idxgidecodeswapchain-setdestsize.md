---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetDestSize
title: IDXGIDecodeSwapChain::SetDestSize (dxgi1_3.h)
description: Sets the size of the destination surface to use for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_setdestsize.htm
tech.root: direct3ddxgi
ms.assetid: BF35FFFE-89C7-4220-9D9F-5BFFE53D3430
ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetDestSize method, IDXGIDecodeSwapChain.SetDestSize, IDXGIDecodeSwapChain::SetDestSize, SetDestSize, SetDestSize method [DXGI], SetDestSize method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setdestsize, dxgi1_3/IDXGIDecodeSwapChain::SetDestSize
ms.topic: method
f1_keywords:
- dxgi1_3/IDXGIDecodeSwapChain.SetDestSize
dev_langs:
- c++
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
req.lib: Dxgi.lib
req.dll: 
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>
 

 

