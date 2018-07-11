---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetSourceRect
title: IDXGIDecodeSwapChain::GetSourceRect
author: windows-sdk-content
description: Gets the source region that is used for the swap chain.
old-location: direct3ddxgi\idxgidecodeswapchain_getsourcerect.htm
old-project: direct3ddxgi
ms.assetid: 67DD1267-997A-4D84-BC91-D124ED1E8946
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetSourceRect, GetSourceRect method [DXGI], GetSourceRect method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetSourceRect method, IDXGIDecodeSwapChain.GetSourceRect, IDXGIDecodeSwapChain::GetSourceRect, direct3ddxgi.idxgidecodeswapchain_getsourcerect, dxgi1_3/IDXGIDecodeSwapChain::GetSourceRect
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
 - IDXGIDecodeSwapChain.GetSourceRect
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDecodeSwapChain::GetSourceRect


## -description


Gets the source region that is used for the swap chain.


## -parameters




### -param pRect [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure 
        that receives the source region for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

