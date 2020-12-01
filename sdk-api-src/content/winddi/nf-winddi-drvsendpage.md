---
UID: NF:winddi.DrvSendPage
title: DrvSendPage function (winddi.h)
description: A printer graphics DLL's DrvSendPage function is called by GDI when it has finished drawing a physical page, so the driver can send the page to the printer.
helpviewer_keywords: ["DrvSendPage","DrvSendPage function [Display Devices]","ddifncs_4211c283-c7c9-493d-b673-0fdc0d8ad04f.xml","display.drvsendpage","winddi/DrvSendPage"]
old-location: display\drvsendpage.htm
tech.root: display
ms.assetid: d9c452e3-3850-4ca2-8114-b3866fbdeba6
ms.date: 12/05/2018
ms.keywords: DrvSendPage, DrvSendPage function [Display Devices], ddifncs_4211c283-c7c9-493d-b673-0fdc0d8ad04f.xml, display.drvsendpage, winddi/DrvSendPage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrvSendPage
 - winddi/DrvSendPage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSendPage
---

# DrvSendPage function


## -description

A printer graphics DLL's <b>DrvSendPage</b> function is called by GDI when it has finished drawing a physical page, so the driver can send the page to the printer.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the drawing surface.

## -returns

If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.

## -remarks

GDI calls <b>DrvSendPage</b> each time it has finished drawing a physical page's image on the drawing surface. The function is responsible for calling <a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a> to send the image to the printer, and for performing end-of-page operations, such as ejecting the page.


<a href="/windows-hardware/drivers/print/printer-graphics-dll">Printer graphics DLLs</a> using GDI-managed surfaces are typically implemented so that for pages that are banded, the image for each band is sent to the printer by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a> function. 

Additionally, if a printer graphics DLL is using a <a href="/windows-hardware/drivers/">device-managed surface</a>, the <b>DrvSendPage</b> function typically only needs to perform end-of-page operations, because the image is sent to the printer as it is drawn.

If there is a potential for this function to take a long time to execute, it should call <a href="/windows/desktop/api/winddi/nf-winddi-engcheckabort">EngCheckAbort</a> every five seconds. If <b>EngCheckAbort</b> returns <b>TRUE</b>, <b>DrvSendPage</b> should terminate its operation and return <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstartpage">DrvStartPage</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engcheckabort">EngCheckAbort</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a>