---
UID: NF:dxgi1_2.IDXGISwapChain1.GetHwnd
title: IDXGISwapChain1::GetHwnd
author: windows-sdk-content
description: Retrieves the underlying HWND for this swap-chain object.
old-location: direct3ddxgi\idxgiswapchain1_gethwnd.htm
tech.root: direct3ddxgi
ms.assetid: C1690710-FA63-4841-B3E2-68200E0B7B23
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetHwnd, GetHwnd method [DXGI], GetHwnd method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetHwnd method, IDXGISwapChain1.GetHwnd, IDXGISwapChain1::GetHwnd, direct3ddxgi.idxgiswapchain1_gethwnd, dxgi1_2/IDXGISwapChain1::GetHwnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps only]
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
 - IDXGISwapChain1.GetHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain1::GetHwnd


## -description


Retrieves the underlying <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> for this swap-chain object.


## -parameters




### -param pHwnd [out]

A pointer to a variable that receives the <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> for the swap-chain object.


## -returns



Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.

If <i>pHwnd</i> receives <b>NULL</b> (that is, the swap chain is not <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>-based), <b>GetHwnd</b> returns <a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a>.




## -remarks



Applications call the  <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a> method to create a swap chain that is associated with an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

