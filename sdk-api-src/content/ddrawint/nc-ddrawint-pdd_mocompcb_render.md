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

# PDD_MOCOMPCB_RENDER callback function


## -description


The <b>DdMoCompRender</b> callback function tells the driver what macroblocks to render by specifying the surfaces containing the macroblocks, the offsets in each surface where the macroblocks exist, and the size of the macroblock data to be rendered. 


## -parameters




### -param Arg1








#### - lpRenderData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551693">DD_RENDERMOCOMPDATA</a> structure that contains the information needed to render a frame. 


## -returns



<b>DdMoCompRender</b> returns one of the following callback codes:




## -remarks



DirectDraw drivers that support motion compensation must implement <b>DdMoCompRender</b>.

<b>DdMoCompRender</b> can be called multiple times between the <a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a> and <a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a> sequence.

If a previous render operation is not yet finished, the driver should fail the call by setting the <b>ddRVal</b> member of the DD_RENDERMOCOMPDATA structure at <i>lpRenderData</i> to DDERR_WASSTILLDRAWING and returning DDHAL_DRIVER_HANDLED. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551693">DD_RENDERMOCOMPDATA</a>



<a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a>



<a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a>
 

 

