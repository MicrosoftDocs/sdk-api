---
UID: NF:dxgi1_3.IDXGISwapChain2.GetMatrixTransform
title: IDXGISwapChain2::GetMatrixTransform
author: windows-sdk-content
description: Gets the transform matrix that will be applied to a composition swap chain upon the next present.
old-location: direct3ddxgi\idxgiswapchain2_getmatrixtransform.htm
tech.root: direct3ddxgi
ms.assetid: 90302283-BB0A-44A9-8CD2-591571EF74ED
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMatrixTransform, GetMatrixTransform method [DXGI], GetMatrixTransform method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetMatrixTransform method, IDXGISwapChain2.GetMatrixTransform, IDXGISwapChain2::GetMatrixTransform, direct3ddxgi.idxgiswapchain2_getmatrixtransform, dxgi1_3/IDXGISwapChain2::GetMatrixTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2.GetMatrixTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain2::GetMatrixTransform


## -description


Gets the transform matrix that will be applied to a composition swap chain upon the next present. 

Starting with Windows 8.1, Windows Store apps are able to place DirectX swap chain visuals in XAML pages using the <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a> element, which can be placed and sized arbitrarily. This exposes the DirectX swap chain visuals to touch scaling and translation scenarios using touch UI. The <b>GetMatrixTransform</b> and  <a href="https://msdn.microsoft.com/AAED8A59-3190-49A0-93AA-F5CAF9088877">SetMatrixTransform</a> methods are used to synchronize scaling of the DirectX swap chain with its associated <b>SwapChainPanel</b> element. Only simple scale/translation elements in the matrix are allowed – the call will fail if the matrix contains skew/rotation elements.


## -parameters




### -param pMatrix [out]

The transform matrix currently used for swap chain scaling and translation.


## -returns



<b>GetMatrixTransform</b> returns:
        <ul>
<li>S_OK if it successfully retrieves the transform matrix.</li>
<li>DXGI_ERROR_INVALID_CALL if the method is called on a swap chain that was not created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a> topic.</li>
</ul>





## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=311761">DirectX foreground swap chains sample</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/AAED8A59-3190-49A0-93AA-F5CAF9088877">SetMatrixTransform</a>
 

 

