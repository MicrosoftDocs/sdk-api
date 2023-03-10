---
UID: NF:winddi.DrvEnableDirectDraw
title: DrvEnableDirectDraw function (winddi.h)
description: The DrvEnableDirectDraw function enables hardware for DirectDraw use.
helpviewer_keywords: ["DrvEnableDirectDraw","DrvEnableDirectDraw function [Display Devices]","ddfncs_259dc59e-2e2c-4cdb-9d79-08e42fd5bc91.xml","display.drvenabledirectdraw","winddi/DrvEnableDirectDraw"]
old-location: display\drvenabledirectdraw.htm
tech.root: display
ms.assetid: eb7e8775-d0ff-42af-8266-5171902eac22
ms.date: 12/05/2018
ms.keywords: DrvEnableDirectDraw, DrvEnableDirectDraw function [Display Devices], ddfncs_259dc59e-2e2c-4cdb-9d79-08e42fd5bc91.xml, display.drvenabledirectdraw, winddi/DrvEnableDirectDraw
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
 - DrvEnableDirectDraw
 - winddi/DrvEnableDirectDraw
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
 - DrvEnableDirectDraw
---

# DrvEnableDirectDraw function


## -description

The <b>DrvEnableDirectDraw</b> function enables hardware for DirectDraw use.

## -parameters

### -param dhpdev

Handle to the <a href="/windows-hardware/drivers/">PDEV</a> returned by the driver's <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a> routine.

### -param pCallBacks

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_callbacks">DD_CALLBACKS</a> structure to be initialized by the driver.

### -param pSurfaceCallBacks

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a> structure to be initialized by the driver.

### -param pPaletteCallBacks

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a> structure to be initialized by the driver.

## -returns

<b>DrvEnableDirectDraw</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

GDI calls the driver's <b>DrvEnableDirectDraw</b> function to obtain pointers to the DirectDraw callbacks that the driver supports. The driver should set the function pointer members of <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_callbacks">DD_CALLBACKS</a>, <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>, and <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a> to point to those functions that it implements. A driver should also set the corresponding bitfields in the <b>dwFlags</b> members of these structures for all supported callbacks.

A driver's <b>DrvEnableDirectDraw</b> implementation can also dedicate hardware resources such as display memory for use by DirectDraw only.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_callbacks">DD_CALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a>



<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdisabledirectdraw">DrvDisableDirectDraw</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvgetdirectdrawinfo">DrvGetDirectDrawInfo</a>