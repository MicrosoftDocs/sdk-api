---
UID: NF:winddi.DrvDisableSurface
title: DrvDisableSurface function (winddi.h)
description: The DrvDisableSurface function is used by GDI to notify a driver that the surface created by DrvEnableSurface for the current device is no longer needed.
helpviewer_keywords: ["DrvDisableSurface","DrvDisableSurface function [Display Devices]","ddifncs_1b5543ca-2860-4383-a2a7-a73adc5cf2a4.xml","display.drvdisablesurface","winddi/DrvDisableSurface"]
old-location: display\drvdisablesurface.htm
tech.root: display
ms.assetid: 18714107-7287-4d50-a2f9-b5d72f111f8b
ms.date: 12/05/2018
ms.keywords: DrvDisableSurface, DrvDisableSurface function [Display Devices], ddifncs_1b5543ca-2860-4383-a2a7-a73adc5cf2a4.xml, display.drvdisablesurface, winddi/DrvDisableSurface
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
 - DrvDisableSurface
 - winddi/DrvDisableSurface
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
 - DrvDisableSurface
---

# DrvDisableSurface function


## -description

The <b>DrvDisableSurface</b> function is used by GDI to notify a driver that the surface created by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a> for the current device is no longer needed.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a>. This is the handle to the device whose surface is to be released.

## -remarks

The driver should free any memory and resources used by the surface associated with the PDEV as soon as the physical device is disabled.

If the driver has been disabled by a call to <a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a>, the driver must not access the hardware during <b>DrvDisableSurface</b> because another active PDEV might be in use. Any necessary hardware changes should have been performed during the call to <b>DrvAssertMode</b>. A driver should keep track of whether it has been disabled by <b>DrvAssertMode</b> so that it can perform proper cleanup operations in <b>DrvDisableSurface</b>.

If the physical device has an enabled surface, GDI calls <b>DrvDisableSurface</b> before calling <a href="/windows/desktop/api/winddi/nf-winddi-drvdisablepdev">DrvDisablePDEV</a>.

<b>DrvDisableSurface</b> is required for graphics drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvassertmode">DrvAssertMode</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdisabledriver">DrvDisableDriver</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvdisablepdev">DrvDisablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvenablesurface">DrvEnableSurface</a>