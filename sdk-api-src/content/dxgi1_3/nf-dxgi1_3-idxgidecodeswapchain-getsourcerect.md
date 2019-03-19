---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetSourceRect
title: IDXGIDecodeSwapChain::GetSourceRect (dxgi1_3.h)
author: windows-sdk-content
description: Gets the source region that is used for the swap chain.
old-location: direct3ddxgi\idxgidecodeswapchain_getsourcerect.htm
tech.root: direct3ddxgi
ms.assetid: 67DD1267-997A-4D84-BC91-D124ED1E8946
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSourceRect, GetSourceRect method [DXGI], GetSourceRect method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetSourceRect method, IDXGIDecodeSwapChain.GetSourceRect, IDXGIDecodeSwapChain::GetSourceRect, direct3ddxgi.idxgidecodeswapchain_getsourcerect, dxgi1_3/IDXGIDecodeSwapChain::GetSourceRect
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
 - IDXGIDecodeSwapChain.GetSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGIDecodeSwapChain::GetSourceRect


## -description


Gets the source region that is used for the swap chain.


## -parameters




### -param pRect [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure 
        that receives the source region for the swap chain.


## -returns



This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/814EDDA6-EFEA-4281-BE06-9FF8822B4927">IDXGIDecodeSwapChain</a>
 

 

