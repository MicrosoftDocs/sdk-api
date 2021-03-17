---
UID: NF:winddi.DrvStartPage
title: DrvStartPage function (winddi.h)
description: The DrvStartPage function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering.
helpviewer_keywords: ["DrvStartPage","DrvStartPage function [Display Devices]","ddifncs_eef4f1da-1923-4282-82d2-ac1ab5386ab9.xml","display.drvstartpage","winddi/DrvStartPage"]
old-location: display\drvstartpage.htm
tech.root: display
ms.assetid: 31e42524-de9a-459a-95a7-94b2597c3cd8
ms.date: 12/05/2018
ms.keywords: DrvStartPage, DrvStartPage function [Display Devices], ddifncs_eef4f1da-1923-4282-82d2-ac1ab5386ab9.xml, display.drvstartpage, winddi/DrvStartPage
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
 - DrvStartPage
 - winddi/DrvStartPage
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
 - DrvStartPage
---

# DrvStartPage function


## -description

The <b>DrvStartPage</b> function is called by GDI when it is ready to start sending the contents of a physical page to the driver for rendering.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure.

## -returns

If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.

## -remarks

A <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> must provide a <b>DrvStartPage</b> function. The function is called before each physical page of a print job is rendered. (A physical page can contain one or more document pages.)

Typically the function is used for sending control sequences to printer hardware, before a page is printed, by calling GDI's <a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a> function. The function can also perform internal, page-specific initialization operations for the printer graphics DLL.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvsendpage">DrvSendPage</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a>