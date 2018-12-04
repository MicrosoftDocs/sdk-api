---
UID: NF:dxgi1_2.IDXGISwapChain1.GetRestrictToOutput
title: IDXGISwapChain1::GetRestrictToOutput
author: windows-sdk-content
description: Gets the output (the display monitor) to which you can restrict the contents of a present operation.
old-location: direct3ddxgi\idxgiswapchain1_getrestricttooutput.htm
tech.root: direct3ddxgi
ms.assetid: 024176FA-BD3B-4410-9342-B8FA2C5B18F6
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetRestrictToOutput, GetRestrictToOutput method [DXGI], GetRestrictToOutput method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetRestrictToOutput method, IDXGISwapChain1.GetRestrictToOutput, IDXGISwapChain1::GetRestrictToOutput, direct3ddxgi.idxgiswapchain1_getrestricttooutput, dxgi1_2/IDXGISwapChain1::GetRestrictToOutput
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDXGISwapChain1.GetRestrictToOutput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain1::GetRestrictToOutput


## -description


Gets the output (the display monitor) to which you can restrict the contents of a present operation.


## -parameters




### -param ppRestrictToOutput [out]

 A pointer to a buffer that receives a pointer to the <a href="https://msdn.microsoft.com/c641995e-a4d9-4bfb-bdc0-7ffbe77c3599">IDXGIOutput</a> interface for the restrict-to output. An application passes this pointer to <b>IDXGIOutput</b> in a call to the  <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or  <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a> method to create the swap chain.


## -returns



Returns S_OK if the restrict-to output was successfully retrieved; otherwise, returns E_INVALIDARG if the pointer is invalid.




## -remarks



If the method succeeds, the runtime fills the buffer at <i>ppRestrictToOutput</i> with a pointer to the restrict-to output interface. This restrict-to output interface has its reference count incremented. When you are finished with it, be sure to release the interface to avoid a memory leak.

The output is also owned by the adapter on which the swap chain's device was created.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

