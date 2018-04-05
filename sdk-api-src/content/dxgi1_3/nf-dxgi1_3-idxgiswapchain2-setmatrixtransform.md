---
UID: NF:dxgi1_3.IDXGISwapChain2.SetMatrixTransform
title: IDXGISwapChain2::SetMatrixTransform method
author: windows-driver-content
description: Sets the transform matrix that will be applied to a composition swap chain upon the next present.
old-location: direct3ddxgi\idxgiswapchain2_setmatrixtransform.htm
old-project: direct3ddxgi
ms.assetid: AAED8A59-3190-49A0-93AA-F5CAF9088877
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGISwapChain2, IDXGISwapChain2 interface [DXGI], SetMatrixTransform method, IDXGISwapChain2::SetMatrixTransform, SetMatrixTransform method [DXGI], SetMatrixTransform method [DXGI], IDXGISwapChain2 interface, SetMatrixTransform,IDXGISwapChain2.SetMatrixTransform, direct3ddxgi.idxgiswapchain2_setmatrixtransform, dxgi1_3/IDXGISwapChain2::SetMatrixTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dxgi.lib
-	dxgi.dll
api_name:
-	IDXGISwapChain2.SetMatrixTransform
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain2::SetMatrixTransform method


## -description


Sets the transform matrix that will be applied to a composition swap chain upon the next present. 

Starting with Windows 8.1, Windows Store apps are able to place DirectX swap chain visuals in XAML pages using the <a href="https://msdn.microsoft.com/e99a6d0f-d556-4aaa-853a-366853614560">SwapChainPanel</a> element, which can be placed and sized arbitrarily. This exposes the DirectX swap chain visuals to touch scaling and translation scenarios using touch UI. The <a href="https://msdn.microsoft.com/90302283-BB0A-44A9-8CD2-591571EF74ED">GetMatrixTransform</a> and  <b>SetMatrixTransform</b> methods are used to synchronize scaling of the DirectX swap chain with its associated <b>SwapChainPanel</b> element. Only simple scale/translation elements in the matrix are allowed – the call will fail if the matrix contains skew/rotation elements.


## -parameters




### -param pMatrix

The transform matrix to use for swap chain scaling and translation. This function can only be used with composition swap chains created by <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>. Only scale and translation components are allowed in the matrix.


## -returns



<b>SetMatrixTransform</b> returns:
        <ul>
<li>S_OK if it successfully retrieves the transform matrix.</li>
<li>E_INVALIDARG if the <i>pMatrix</i> parameter is incorrect, for example, <i>pMatrix</i> is NULL or the matrix represented by <a href="https://msdn.microsoft.com/5EA0FAD4-5F19-4E5A-97D4-11AE750E8560">DXGI_MATRIX_3X2_F</a> includes components other than scale and translation.</li>
<li>DXGI_ERROR_INVALID_CALL if the method is called on a swap chain that was not created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">CreateSwapChainForComposition</a>.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>





## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=311761">DirectX foreground swap chains sample</a>



<a href="https://msdn.microsoft.com/90302283-BB0A-44A9-8CD2-591571EF74ED">GetMatrixTransform</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>
 

 

