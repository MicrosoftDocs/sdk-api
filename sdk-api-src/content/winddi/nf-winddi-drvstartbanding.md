---
UID: NF:winddi.DrvStartBanding
title: DrvStartBanding function (winddi.h)
description: The DrvStartBanding function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.
helpviewer_keywords: ["DrvStartBanding","DrvStartBanding function [Display Devices]","ddifncs_d0cd5c63-cf46-472a-be6c-8d9dd124a2b2.xml","display.drvstartbanding","winddi/DrvStartBanding"]
old-location: display\drvstartbanding.htm
tech.root: display
ms.assetid: c9006dd1-055b-4fb0-92e8-c7b6bc294941
ms.date: 12/05/2018
ms.keywords: DrvStartBanding, DrvStartBanding function [Display Devices], ddifncs_d0cd5c63-cf46-472a-be6c-8d9dd124a2b2.xml, display.drvstartbanding, winddi/DrvStartBanding
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
 - DrvStartBanding
 - winddi/DrvStartBanding
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
 - DrvStartBanding
---

# DrvStartBanding function


## -description

The <b>DrvStartBanding</b> function is called by GDI when it is ready to start sending bands of a physical page to the driver for rendering.

## -parameters

### -param pso [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure, which identifies the banding surface.

### -param pptl [in]

Caller-supplied pointer to a <a href="/windows/desktop/api/windef/ns-windef-pointl">POINTL</a> structure to receive the function-supplied origin of the first band.

## -returns

If the operation succeeds, the function should return <b>TRUE</b>. Otherwise, it should call the Win32 <b>SetLastError</b> function to set an error code, and then return <b>FALSE</b>.

## -remarks

If a printer graphics DLL uses GDI-managed surfaces, and if it supports surface banding, it must provide a <a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a> function. GDI calls <b>DrvStartBanding</b> only if the printer graphics DLL's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a> function previously called <a href="/windows/desktop/api/winddi/nf-winddi-engmarkbandingsurface">EngMarkBandingSurface</a> to specify a banding surface.

The <b>DrvStartBanding</b> function's purpose is to allow the printer graphics DLL to perform any initializations needed before banding operations begin on a physical page, and to provide GDI with the indices of the first band's origin.

The <b>DrvStartBanding</b> function is called once per page. Each time GDI has finished drawing a band, it calls <a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a> so the driver can send the band to the printer.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvnextband">DrvNextBand</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engmarkbandingsurface">EngMarkBandingSurface</a>