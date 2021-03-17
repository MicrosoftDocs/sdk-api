---
UID: NF:winddi.DrvNextBand
title: DrvNextBand function (winddi.h)
description: The DrvNextBand function is called by GDI when it has finished drawing a band for a physical page, so the driver can send the next band to the printer.
helpviewer_keywords: ["DrvNextBand","DrvNextBand function [Display Devices]","ddifncs_dc66e17a-f2da-45cc-bc1a-8058006c6922.xml","display.drvnextband","winddi/DrvNextBand"]
old-location: display\drvnextband.htm
tech.root: display
ms.assetid: 7c02d32b-6c95-4dd5-b9cf-2f64ba78f25a
ms.date: 12/05/2018
ms.keywords: DrvNextBand, DrvNextBand function [Display Devices], ddifncs_dc66e17a-f2da-45cc-bc1a-8058006c6922.xml, display.drvnextband, winddi/DrvNextBand
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
 - DrvNextBand
 - winddi/DrvNextBand
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
 - DrvNextBand
---

# DrvNextBand function


## -description

The <b>DrvNextBand</b> function is called by GDI when it has finished drawing a band for a physical page, so the driver can send the next band to the printer.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure, which identifies the banding surface.

### -param pptl [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure to receive the function-supplied origin of the next band.

## -returns

If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.

## -remarks

If a <a href="/windows-hardware/drivers/print/printer-graphics-dll">printer graphics DLL</a> uses GDI-managed surfaces, and if it supports surface banding, it must provide a <b>DrvNextBand</b> function. GDI calls <b>DrvNextBand</b> each time it has finished drawing the portion of the page's image that can be contained on the band's surface. The surface used by GDI for drawing is one that the driver previously specified by calling <a href="/windows/desktop/api/winddi/nf-winddi-engmarkbandingsurface">EngMarkBandingSurface</a>. The function should send the image to the printer by calling <a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a>, and it should return the indices of the next band's origin in the POINTL structure pointed to by <i>pptl</i>.

After all of a physical page's bands have been drawn, the function should set both members of the POINTL structure pointed to by <i>pptl</i> to -1.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvstartbanding">DrvStartBanding</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmarkbandingsurface">EngMarkBandingSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engwriteprinter">EngWritePrinter</a>