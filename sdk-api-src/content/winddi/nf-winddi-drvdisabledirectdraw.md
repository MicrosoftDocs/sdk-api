---
UID: NF:winddi.DrvDisableDirectDraw
title: DrvDisableDirectDraw function
author: windows-sdk-content
description: The DrvDisableDirectDraw function disables hardware for DirectDraw use.
old-location: display\drvdisabledirectdraw.htm
tech.root: display
ms.assetid: 7675019e-ac05-40e8-a934-a0928800ebe3
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: DrvDisableDirectDraw, DrvDisableDirectDraw function [Display Devices], ddfncs_7abbe471-0671-4e98-8eba-ceb25216d961.xml, display.drvdisabledirectdraw, winddi/DrvDisableDirectDraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvDisableDirectDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvDisableDirectDraw function


## -description


The <b>DrvDisableDirectDraw</b> function disables hardware for DirectDraw use.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> that was returned by the driver's <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a> routine.


## -returns



None




## -remarks



GDI calls the driver's <b>DrvDisableDirectDraw</b> function when the last DirectDraw application has finished running. A driver's <b>DrvDisableDirectDraw</b> implementation should clean up any software resources and reclaim any hardware resources that the driver dedicated to DirectDraw in its <a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a> function.

<b>DrvDisableDirectDraw</b> can be called with a disabled <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. A PDEV is disabled or enabled by calling the display driver's <a href="https://msdn.microsoft.com/29846ffd-b721-4d61-9983-07a2575f9fe8">DrvAssertMode</a> function. See <a href="https://msdn.microsoft.com/f7badbe8-b24f-438a-8937-95bb98de6310">Managing PDEVs</a> for more information. 




## -see-also




<a href="https://msdn.microsoft.com/eb7e8775-d0ff-42af-8266-5171902eac22">DrvEnableDirectDraw</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>
 

 

