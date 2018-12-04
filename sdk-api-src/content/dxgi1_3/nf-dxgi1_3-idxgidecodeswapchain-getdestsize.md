---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetDestSize
title: IDXGIDecodeSwapChain::GetDestSize
author: windows-sdk-content
description: Gets the size of the destination surface to use for the video processing blit operation.
old-location: direct3ddxgi\idxgidecodeswapchain_getdestsize.htm
tech.root: direct3ddxgi
ms.assetid: FA01A6C1-7731-4B30-845F-4C2514B6AD77
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetDestSize, GetDestSize method [DXGI], GetDestSize method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetDestSize method, IDXGIDecodeSwapChain.GetDestSize, IDXGIDecodeSwapChain::GetDestSize, direct3ddxgi.idxgidecodeswapchain_getdestsize, dxgi1_3/IDXGIDecodeSwapChain::GetDestSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDXGIDecodeSwapChain.GetDestSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDecodeSwapChain::GetDestSize


## -description


Gets the size of the destination surface to use for the video processing blit operation.


## -parameters




### -param pWidth [out]

A pointer to a variable that receives the width in pixels.


### -param pHeight [out]

A pointer to a variable that receives the height in pixels.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

