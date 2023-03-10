---
UID: NF:winddi.DrvResetPDEV
title: DrvResetPDEV function (winddi.h)
description: The DrvResetPDEV function allows a graphics driver to transfer the state of the driver from an old PDEV structure to a new PDEV structure when a Win32 application calls ResetDC.
helpviewer_keywords: ["DrvResetPDEV","DrvResetPDEV function [Display Devices]","ddifncs_839f09e0-67dc-4c1f-a17b-dd0fd5316258.xml","display.drvresetpdev","winddi/DrvResetPDEV"]
old-location: display\drvresetpdev.htm
tech.root: display
ms.assetid: 8e530874-7774-4f8f-852c-001b2ce4a707
ms.date: 12/05/2018
ms.keywords: DrvResetPDEV, DrvResetPDEV function [Display Devices], ddifncs_839f09e0-67dc-4c1f-a17b-dd0fd5316258.xml, display.drvresetpdev, winddi/DrvResetPDEV
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
 - DrvResetPDEV
 - winddi/DrvResetPDEV
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
 - DrvResetPDEV
---

# DrvResetPDEV function


## -description

The <b>DrvResetPDEV</b> function allows a graphics driver to transfer the state of the driver from an old <a href="/windows-hardware/drivers/">PDEV</a> structure to a new PDEV structure when a Win32 application calls <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a>.

## -parameters

### -param dhpdevOld

Caller-supplied handle to the original device PDEV structure. This handle was previously provided by the driver as a return value for <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param dhpdevNew

Caller-supplied handle to the new PDEV structure.

## -returns

This return value is <b>TRUE</b> if the function is successful. Otherwise it is <b>FALSE</b>, and an error code is logged.

## -remarks

A graphics driver's <b>DrvResetPDEV</b> function should be used for modifying the contents of a new PDEV structure, based on the contents of the old (currently in use) PDEV structure.

OpenGL display drivers that need to know about mode changes should implement <b>DrvResetPDEV</b>. Otherwise, all other display drivers typically do not need to implement this function.

<h3><a id="Note__The_following_information_pertains_to_printer_graphics_DLLs."></a><a id="note__the_following_information_pertains_to_printer_graphics_dlls."></a><a id="NOTE__THE_FOLLOWING_INFORMATION_PERTAINS_TO_PRINTER_GRAPHICS_DLLS."></a>Note  The following information pertains to printer graphics DLLs.</h3>
The function is called as a result of an application's call to the Win32 <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a> function, which in turn causes GDI to call the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> to obtain a new PDEV structure. Because the driver can modify a PDEV structure's contents during the rendering of a print job, the <b>DrvResetPDEV</b> function allows the driver to transfer these modifications from the old PDEV structure to the new one.

Examples of the types of information that a printer graphics DLL might want to add to the new PDEV structure are pointers to cached font files, or flags indicating whether page initialization should (or should not) take place the next time <a href="/windows/desktop/api/winddi/nf-winddi-drvstartdoc">DrvStartDoc</a> or <a href="/windows/desktop/api/winddi/nf-winddi-drvstartpage">DrvStartPage</a> is called. 

If <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a> is called during the rendering of a print document, the printer graphics DLL receives the following sequence of calls:


```
    dhpdevNew = DrvEnablePDEV();
    DrvResetPDEV(dhpdevOld, dhpdevNew);
    DrvDisableSurface(dhpdevOld);
    DrvDisablePDEV(dhpdevOld);
    DrvEnableSurface(dhpdevNew);
    DrvStartDoc(dhpdevNew);
```


If  <a href="/windows/desktop/api/wingdi/nf-wingdi-resetdca">ResetDC</a> is called between documents there is no surface associated with the PDEV, so only the following sequence of calls is made:


```
    dhpdevNew = DrvEnablePDEV();
    DrvResetPDEV(dhpdevOld,dhpdevNew);
    DrvDisablePDEV(dhpdevOld);
```

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvdisablepdev">DrvDisablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdisablesurface">DrvDisableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstartdoc">DrvStartDoc</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstartpage">DrvStartPage</a>