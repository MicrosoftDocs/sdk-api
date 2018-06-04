---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>





## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=311761">DirectX foreground swap chains sample</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/AAED8A59-3190-49A0-93AA-F5CAF9088877">SetMatrixTransform</a>
 

 

