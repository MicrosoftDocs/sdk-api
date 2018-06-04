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
 

 

