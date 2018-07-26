---
UID: NF:dxgi1_2.IDXGISwapChain1.GetDesc1
title: IDXGISwapChain1::GetDesc1
author: windows-sdk-content
description: Gets a description of the swap chain.
old-location: direct3ddxgi\idxgiswapchain1_getdesc1.htm
old-project: direct3ddxgi
ms.assetid: 86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetDesc1 method, IDXGISwapChain1.GetDesc1, IDXGISwapChain1::GetDesc1, direct3ddxgi.idxgiswapchain1_getdesc1, dxgi1_2/IDXGISwapChain1::GetDesc1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: DXGI_OFFER_RESOURCE_PRIORITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.GetDesc1
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain1::GetDesc1


## -description


Gets a description of the swap chain.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/38B302DF-5617-4195-8E4A-619D75188AD5">DXGI_SWAP_CHAIN_DESC1</a>  structure that describes the swap chain.


## -returns



Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

