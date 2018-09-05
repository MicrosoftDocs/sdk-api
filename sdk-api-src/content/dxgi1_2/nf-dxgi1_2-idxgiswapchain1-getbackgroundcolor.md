---
UID: NF:dxgi1_2.IDXGISwapChain1.GetBackgroundColor
title: IDXGISwapChain1::GetBackgroundColor
author: windows-sdk-content
description: Retrieves the background color of the swap chain.
old-location: direct3ddxgi\idxgiswapchain1_getbackgroundcolor.htm
old-project: direct3ddxgi
ms.assetid: AF10BAF1-5C49-45E7-B776-3EB606C02E10
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetBackgroundColor, GetBackgroundColor method [DXGI], GetBackgroundColor method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetBackgroundColor method, IDXGISwapChain1.GetBackgroundColor, IDXGISwapChain1::GetBackgroundColor, direct3ddxgi.idxgiswapchain1_getbackgroundcolor, dxgi1_2/IDXGISwapChain1::GetBackgroundColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxgi1_2.h
req.include-header: 
req.redist: 
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
 - IDXGISwapChain1.GetBackgroundColor
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain1::GetBackgroundColor


## -description


Retrieves the background color of the swap chain.


## -parameters




### -param pColor [out]

A pointer to a <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> structure that receives the background color of the swap chain.


## -returns



<b>GetBackgroundColor</b> returns:
        <ul>
<li>S_OK if it successfully retrieves the background color.</li>
<li>
<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a> if the <i>pColor</i> parameter is invalid, for example, <i>pColor</i> is NULL.</li>
<li>Possibly other error codes that are described in the <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a> topic.</li>
</ul>





## -remarks



<div class="alert"><b>Note</b>  The background color that <b>GetBackgroundColor</b> retrieves does not indicate what the screen currently displays. The background color indicates what the screen will display with your next call to the <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> method. The default value of the background color is black with full opacity: 0,0,0,1.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>



<a href="https://msdn.microsoft.com/E46CA219-303F-40D4-8C62-6241C9199BA0">IDXGISwapChain1::SetBackgroundColor</a>
 

 

