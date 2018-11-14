---
UID: NF:dxgi1_2.IDXGISwapChain1.SetRotation
title: IDXGISwapChain1::SetRotation
author: windows-sdk-content
description: Sets the rotation of the back buffers for the swap chain.
old-location: direct3ddxgi\idxgiswapchain1_setrotation.htm
tech.root: direct3ddxgi
ms.assetid: D1CD2B20-FC7E-4141-A828-96E070A63F4A
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],SetRotation method, IDXGISwapChain1.SetRotation, IDXGISwapChain1::SetRotation, SetRotation, SetRotation method [DXGI], SetRotation method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_setrotation, dxgi1_2/IDXGISwapChain1::SetRotation
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
 - IDXGISwapChain1.SetRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dxgi1_2.h
: 
- IDXGISwapChain1.SetRotation
: 
---

# IDXGISwapChain1::SetRotation


## -description


Sets the rotation of the back buffers for the swap chain.


## -parameters




### -param Rotation [in]

A <a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a>-typed value that specifies how to set the rotation of the back buffers for the swap chain.


## -returns



<b>SetRotation</b> returns:
        <ul>
<li>S_OK if it successfully set the rotation.</li>
<li>DXGI_ERROR_INVALID_CALL if the swap chain is bit-block transfer (bitblt) model. The swap chain must be flip model to successfully call <b>SetRotation</b>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>SetRotation</b> fails with DXGI_ERROR_INVALID_CALL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



You can only use <b>SetRotation</b> to rotate the back buffers for flip-model swap chains that you present in windowed mode. 

<b>SetRotation</b> isn't supported for rotating the back buffers for flip-model swap chains that you present in full-screen mode. In this situation, <b>SetRotation</b> doesn't fail, but you must ensure that you specify no rotation (<a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION_IDENTITY</a>) for the swap chain. Otherwise, when you call <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> or <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> to present a frame,  the presentation fails.




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

