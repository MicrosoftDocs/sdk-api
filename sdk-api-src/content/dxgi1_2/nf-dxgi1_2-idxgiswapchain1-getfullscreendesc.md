---
UID: NF:dxgi1_2.IDXGISwapChain1.GetFullscreenDesc
title: IDXGISwapChain1::GetFullscreenDesc
author: windows-sdk-content
description: Gets a description of a full-screen swap chain.
old-location: direct3ddxgi\idxgiswapchain1_getfullscreendesc.htm
tech.root: direct3ddxgi
ms.assetid: 6056239A-B3CA-4C70-9081-499B0AAEFBEF
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetFullscreenDesc, GetFullscreenDesc method [DXGI], GetFullscreenDesc method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetFullscreenDesc method, IDXGISwapChain1.GetFullscreenDesc, IDXGISwapChain1::GetFullscreenDesc, direct3ddxgi.idxgiswapchain1_getfullscreendesc, dxgi1_2/IDXGISwapChain1::GetFullscreenDesc
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
 - IDXGISwapChain1.GetFullscreenDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain1::GetFullscreenDesc


## -description


Gets a description of a full-screen swap chain.


## -parameters




### -param pDesc [out]

A pointer to a <a href="https://msdn.microsoft.com/0EE5683E-0623-4FD7-A77F-B64F90A25C6A">DXGI_SWAP_CHAIN_FULLSCREEN_DESC</a>  structure that describes the full-screen swap chain.


## -returns



<b>GetFullscreenDesc</b> returns:
        <ul>
<li>S_OK if it successfully retrieved the description of the full-screen swap chain.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a>  for non-<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a> swap chains or if <i>pDesc</i> is <b>NULL</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic. </li>
</ul>





## -remarks



The semantics of <b>GetFullscreenDesc</b> are identical to that of the <a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">IDXGISwapchain::GetDesc</a> method for <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>-based swap chains.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

