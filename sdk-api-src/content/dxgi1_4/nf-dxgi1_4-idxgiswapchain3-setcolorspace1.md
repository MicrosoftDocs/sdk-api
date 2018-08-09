---
UID: NF:dxgi1_4.IDXGISwapChain3.SetColorSpace1
title: IDXGISwapChain3::SetColorSpace1
author: windows-sdk-content
description: Sets the color space used by the swap chain.
old-location: direct3ddxgi\idxgiswapchain3_setcolorspace1.htm
old-project: direct3ddxgi
ms.assetid: 3B4391A5-C4E0-4D2E-BCEE-5DB635B98CFD
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDXGISwapChain3 interface [DXGI],SetColorSpace1 method, IDXGISwapChain3.SetColorSpace1, IDXGISwapChain3::SetColorSpace1, SetColorSpace1, SetColorSpace1 method [DXGI], SetColorSpace1 method [DXGI],IDXGISwapChain3 interface, direct3ddxgi.idxgiswapchain3_setcolorspace1, dxgi1_4/IDXGISwapChain3::SetColorSpace1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: DXGI_SWAP_CHAIN_COLOR_SPACE_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain3.SetColorSpace1
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain3::SetColorSpace1


## -description


Sets the color space used by the swap chain.


## -parameters




### -param ColorSpace [in]

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

A <a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a>-typed value that specifies the color space to set.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns <b>S_OK</b> on success, or it returns one of the error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.




## -see-also




<a href="https://msdn.microsoft.com/3B91A70D-C635-46DF-871D-F1796D4E50E7">IDXGISwapChain3</a>
 

 

