---
UID: NF:winddi.DrvEnableDirectDraw
title: DrvEnableDirectDraw function
author: windows-sdk-content
description: The DrvEnableDirectDraw function enables hardware for DirectDraw use.
old-location: display\drvenabledirectdraw.htm
tech.root: display
ms.assetid: eb7e8775-d0ff-42af-8266-5171902eac22
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrvEnableDirectDraw, DrvEnableDirectDraw function [Display Devices], ddfncs_259dc59e-2e2c-4cdb-9d79-08e42fd5bc91.xml, display.drvenabledirectdraw, winddi/DrvEnableDirectDraw
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
 - DrvEnableDirectDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvEnableDirectDraw function


## -description


The <b>DrvEnableDirectDraw</b> function enables hardware for DirectDraw use.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> returned by the driver's <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a> routine.


### -param pCallBacks

Points to the <a href="https://msdn.microsoft.com/d68b2772-dca6-417a-8e03-d3b2843fb69d">DD_CALLBACKS</a> structure to be initialized by the driver.


### -param pSurfaceCallBacks

Points to the <a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a> structure to be initialized by the driver.


### -param pPaletteCallBacks

Points to the <a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a> structure to be initialized by the driver.


## -returns



<b>DrvEnableDirectDraw</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



GDI calls the driver's <b>DrvEnableDirectDraw</b> function to obtain pointers to the DirectDraw callbacks that the driver supports. The driver should set the function pointer members of <a href="https://msdn.microsoft.com/d68b2772-dca6-417a-8e03-d3b2843fb69d">DD_CALLBACKS</a>, <a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>, and <a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a> to point to those functions that it implements. A driver should also set the corresponding bitfields in the <b>dwFlags</b> members of these structures for all supported callbacks.

A driver's <b>DrvEnableDirectDraw</b> implementation can also dedicate hardware resources such as display memory for use by DirectDraw only.




## -see-also




<a href="https://msdn.microsoft.com/d68b2772-dca6-417a-8e03-d3b2843fb69d">DD_CALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/7675019e-ac05-40e8-a934-a0928800ebe3">DrvDisableDirectDraw</a>



<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/c6068572-bd73-4faa-b085-9608ebc450ea">DrvGetDirectDrawInfo</a>
 

 

