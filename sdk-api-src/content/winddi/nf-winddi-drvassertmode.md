---
UID: NF:winddi.DrvAssertMode
title: DrvAssertMode function (winddi.h)
description: The DrvAssertMode function sets the mode of the specified physical device to either the mode specified when the PDEV was initialized or to the default mode of the hardware.
helpviewer_keywords: ["DrvAssertMode","DrvAssertMode function [Display Devices]","ddifncs_2ff05b29-d53b-44b9-a7fc-2c050f1ba778.xml","display.drvassertmode","winddi/DrvAssertMode"]
old-location: display\drvassertmode.htm
tech.root: display
ms.assetid: 29846ffd-b721-4d61-9983-07a2575f9fe8
ms.date: 12/05/2018
ms.keywords: DrvAssertMode, DrvAssertMode function [Display Devices], ddifncs_2ff05b29-d53b-44b9-a7fc-2c050f1ba778.xml, display.drvassertmode, winddi/DrvAssertMode
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
 - DrvAssertMode
 - winddi/DrvAssertMode
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
 - DrvAssertMode
---

# DrvAssertMode function


## -description

The <b>DrvAssertMode</b> function sets the mode of the specified physical device to either the mode specified when the PDEV was initialized or to the default mode of the hardware.

## -parameters

### -param dhpdev [in]

Handle to the PDEV describing the hardware mode that should be set when <i>bEnable</i> is <b>TRUE</b>.

### -param bEnable [in]

Specifies the mode to which the hardware is to be set. If this parameter is <b>TRUE</b>, the driver should set the hardware to the original mode specified by the initialized PDEV. Otherwise, if this parameter is <b>FALSE</b>, the driver should set the hardware to its default mode so the video miniport driver can assume control.

## -returns

<b>DrvAssertMode</b> returns <b>TRUE</b> if it successfully changed the display mode; it returns <b>FALSE</b> if it was unable to change the display mode. A driver is permitted to return <b>FALSE</b> from a <b>DrvAssertMode</b> call with <i>bEnable</i> set to <b>FALSE</b>. A driver must return <b>TRUE</b> from a <b>DrvAssertMode</b> call with <i>bEnable</i> set to <b>TRUE</b>; that is, a driver cannot fail enabling a mode that was previously enabled.

## -remarks

GDI calls <b>DrvAssertMode</b> when it is required to switch among multiple desktops on a single display surface. To switch from one PDEV to another, GDI calls <b>DrvAssertMode</b> with the <i>bEnable</i> parameter set to <b>FALSE</b> for one PDEV, and <b>TRUE</b> for the other. To revert to the original PDEV, <b>DrvAssertMode</b> is called with <i>bEnable</i> set to <b>FALSE</b>, followed by another call to <b>DrvAssertMode</b>, with <i>bEnable</i> set to <b>TRUE</b> and <b>dhpdev</b> set to the original PDEV.

If the physical device is palette-managed, GDI will call <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpalette">DrvSetPalette</a> to reset the device's palette. The driver does not then need to keep track of the current pointer state because Window Manager selects the correct pointer shape and moves it to the current position. The console manager ensures that desktops are properly redrawn.

<b>DrvAssertMode</b> must be implemented in display drivers.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvgetmodes">DrvGetModes</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsetpalette">DrvSetPalette</a>