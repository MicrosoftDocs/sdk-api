---
UID: NF:winddi.DrvEnableDirectDraw
title: DrvEnableDirectDraw function
author: windows-driver-content
description: The DrvEnableDirectDraw function enables hardware for DirectDraw use.
old-location: display\drvenabledirectdraw.htm
old-project: display
ms.assetid: eb7e8775-d0ff-42af-8266-5171902eac22
ms.author: windowsdriverdev
ms.date: 4/16/2018
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DrvEnableDirectDraw
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvEnableDirectDraw function


## -description


The <b>DrvEnableDirectDraw</b> function enables hardware for DirectDraw use.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> returned by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a> routine.


### -param pCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a> structure to be initialized by the driver.


### -param pSurfaceCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a> structure to be initialized by the driver.


### -param pPaletteCallBacks

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a> structure to be initialized by the driver.


## -returns



<b>DrvEnableDirectDraw</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.




## -remarks



GDI calls the driver's <b>DrvEnableDirectDraw</b> function to obtain pointers to the DirectDraw callbacks that the driver supports. The driver should set the function pointer members of <a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a> to point to those functions that it implements. A driver should also set the corresponding bitfields in the <b>dwFlags</b> members of these structures for all supported callbacks.

A driver's <b>DrvEnableDirectDraw</b> implementation can also dedicate hardware resources such as display memory for use by DirectDraw only.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550485">DD_CALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556195">DrvDisableDirectDraw</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556229">DrvGetDirectDrawInfo</a>
 

 

