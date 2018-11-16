---
UID: NF:dxgi1_2.IDXGISwapChain1.GetRotation
title: IDXGISwapChain1::GetRotation
author: windows-sdk-content
description: Gets the rotation of the back buffers for the swap chain.
old-location: direct3ddxgi\idxgiswapchain1_getrotation.htm
tech.root: direct3ddxgi
ms.assetid: B4460AF4-20B1-493D-88E4-2ADB304D6D60
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRotation, GetRotation method [DXGI], GetRotation method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetRotation method, IDXGISwapChain1.GetRotation, IDXGISwapChain1::GetRotation, direct3ddxgi.idxgiswapchain1_getrotation, dxgi1_2/IDXGISwapChain1::GetRotation
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
 - IDXGISwapChain1.GetRotation
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
- IDXGISwapChain1.GetRotation
: 
---

# IDXGISwapChain1::GetRotation


## -description


Gets the rotation of the back buffers for the swap chain.


## -parameters




### -param pRotation [out]

A pointer to a variable that receives a <a href="https://msdn.microsoft.com/fcf5bce5-dde1-4d3b-9786-2abf1e18d942">DXGI_MODE_ROTATION</a>-typed value that specifies the rotation of the back buffers for the swap chain.


## -returns



Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>GetRotation</b> fails with DXGI_ERROR_INVALID_CALL. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

