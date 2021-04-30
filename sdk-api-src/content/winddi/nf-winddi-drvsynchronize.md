---
UID: NF:winddi.DrvSynchronize
title: DrvSynchronize function (winddi.h)
description: The DrvSynchronize function informs the driver that GDI needs to access a device-managed surface. This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.
helpviewer_keywords: ["DrvSynchronize","DrvSynchronize function [Display Devices]","ddifncs_dadafaae-d13a-4a52-b179-a8b14a835a24.xml","display.drvsynchronize","winddi/DrvSynchronize"]
old-location: display\drvsynchronize.htm
tech.root: display
ms.assetid: ed9b7db3-1409-4aa6-9ee1-9ece53e747a6
ms.date: 12/05/2018
ms.keywords: DrvSynchronize, DrvSynchronize function [Display Devices], ddifncs_dadafaae-d13a-4a52-b179-a8b14a835a24.xml, display.drvsynchronize, winddi/DrvSynchronize
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
 - DrvSynchronize
 - winddi/DrvSynchronize
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
 - DrvSynchronize
---

# DrvSynchronize function


## -description

The <b>DrvSynchronize</b> function informs the driver that GDI needs to access a device-managed surface. This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.

## -parameters

### -param dhpdev

Handle to the physical device's <a href="/windows-hardware/drivers/">PDEV</a> structure that identifies the device to be synchronized with GDI. This parameter is the device handle returned to GDI by <a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>.

### -param prcl

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure. This parameter should be ignored by the driver.

## -remarks

This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.

<b>DrvSynchronize</b> can be optionally implemented in display drivers. GDI calls this function only if it is hooked by <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>. GDI calls <b>DrvSynchronize</b> just before drawing directly onto the device surface. GDI will call <a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a> instead of <b>DrvSynchronize</b> in drivers that implement both of these functions.

This function should return only when it is safe for GDI to access any device-managed surface. That is, <b>DrvSynchronize</b> should delay returning from the call until all asynchronous drawing operations have been completed by the device's coprocessor, thus indicating that it is safe for GDI to access any device-managed surface.

<b>DrvSynchronize</b> is intended to support devices that use a coprocessor for drawing. Such a device can treat some drawing operations as asynchronous, returning to GDI from the operation before the drawing is complete. If this is the case, it is possible that a subsequent drawing operation will be handled by GDI. In order for GDI to safely access device-managed surfaces, it must have a means of ensuring that any <a href="/windows-hardware/drivers/">asynchronous rendering</a> being done by the device's coprocessor is complete. By calling this function, GDI synchronizes access to a device-managed surface with the driver.

GDI will never call <b>DrvSynchronize</b> for device-managed surfaces. <b>DrvSynchronize</b> is not itself an output function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronizesurface">DrvSynchronizeSurface</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>