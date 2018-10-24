---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetColorSpace
title: IDXGIDecodeSwapChain::SetColorSpace
author: windows-sdk-content
description: Sets the color space used by the swap chain.
old-location: direct3ddxgi\idxgidecodeswapchain_setcolorspace.htm
tech.root: direct3ddxgi
ms.assetid: DE0AA2BF-8E98-4CF4-8CC2-760AB4B8776D
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetColorSpace method, IDXGIDecodeSwapChain.SetColorSpace, IDXGIDecodeSwapChain::SetColorSpace, SetColorSpace, SetColorSpace method [DXGI], SetColorSpace method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setcolorspace, dxgi1_3/IDXGIDecodeSwapChain::SetColorSpace
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
 - IDXGIDecodeSwapChain.SetColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDecodeSwapChain::SetColorSpace


## -description


Sets the color space used by the swap chain.


## -parameters




### -param ColorSpace

A pointer to a combination of <a href="https://msdn.microsoft.com/8BD502DC-39C1-472E-AC29-14A1F7EDB37E">DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the color space to set for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

