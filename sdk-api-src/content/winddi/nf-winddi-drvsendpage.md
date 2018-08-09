---
UID: NF:winddi.DrvSendPage
title: DrvSendPage function
author: windows-sdk-content
description: A printer graphics DLL's DrvSendPage function is called by GDI when it has finished drawing a physical page, so the driver can send the page to the printer.
old-location: display\drvsendpage.htm
old-project: display
ms.assetid: d9c452e3-3850-4ca2-8114-b3866fbdeba6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvSendPage, DrvSendPage function [Display Devices], ddifncs_4211c283-c7c9-493d-b673-0fdc0d8ad04f.xml, display.drvsendpage, winddi/DrvSendPage
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSendPage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvSendPage function


## -description


A printer graphics DLL's <b>DrvSendPage</b> function is called by GDI when it has finished drawing a physical page, so the driver can send the page to the printer.


## -parameters




### -param pso [in]

Caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569901">SURFOBJ</a> structure that describes the drawing surface.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.




## -remarks



GDI calls <b>DrvSendPage</b> each time it has finished drawing a physical page's image on the drawing surface. The function is responsible for calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a> to send the image to the printer, and for performing end-of-page operations, such as ejecting the page.


<a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">Printer graphics DLLs</a> using GDI-managed surfaces are typically implemented so that for pages that are banded, the image for each band is sent to the printer by the driver's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a> function. 

Additionally, if a printer graphics DLL is using a <a href="https://msdn.microsoft.com/86688b5d-575d-42e1-9158-7ffba1aaf1d3">device-managed surface</a>, the <b>DrvSendPage</b> function typically only needs to perform end-of-page operations, because the image is sent to the printer as it is drawn.

If there is a potential for this function to take a long time to execute, it should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564189">EngCheckAbort</a> every five seconds. If <b>EngCheckAbort</b> returns <b>TRUE</b>, <b>DrvSendPage</b> should terminate its operation and return <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556250">DrvNextBand</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556298">DrvStartPage</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564189">EngCheckAbort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565467">EngWritePrinter</a>
 

 

