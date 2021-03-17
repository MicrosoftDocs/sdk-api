---
UID: NF:winddi.DrvMovePointer
title: DrvMovePointer function (winddi.h)
description: The DrvMovePointer function moves the pointer to a new position and ensures that GDI does not interfere with the display of the pointer.
helpviewer_keywords: ["DrvMovePointer","DrvMovePointer function [Display Devices]","ddifncs_4fda6dd1-abd6-45fa-ba92-d20352fe35c5.xml","display.drvmovepointer","winddi/DrvMovePointer"]
old-location: display\drvmovepointer.htm
tech.root: display
ms.assetid: eb117f39-0823-4eb7-8628-fa4399a13ec6
ms.date: 12/05/2018
ms.keywords: DrvMovePointer, DrvMovePointer function [Display Devices], ddifncs_4fda6dd1-abd6-45fa-ba92-d20352fe35c5.xml, display.drvmovepointer, winddi/DrvMovePointer
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
 - DrvMovePointer
 - winddi/DrvMovePointer
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
 - DrvMovePointer
---

# DrvMovePointer function


## -description

The <b>DrvMovePointer</b> function moves the pointer to a new position and ensures that GDI does not interfere with the display of the pointer.

## -parameters

### -param pso [in]

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that describes the surface of a display device.

### -param x [in]

Specify the <i>x</i> coordinate on the display where the driver should position the hot spot of the pointer.

A negative <i>x</i> value indicates that the driver should remove the pointer from the display because drawing is about to occur where it is presently located. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the driver should restore the pointer.

### -param y [in]

Specify the <i>y</i> coordinate on the display where the driver should position the hot spot of the pointer.

When the driver has set the GCAPS_PANNING flag in the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure, a negative <i>y</i> value indicates that GDI is calling this function only to notify the driver of the cursor's current position. The current position can be computed as (<i>x</i>, <i>y</i>+<i>pso</i>-&gt;sizlBitmap.cy). A driver that does not set the GCAPS_PANNING flag will never receive a negative <i>y</i> coordinate.

### -param prcl [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.

## -remarks

Drivers sometimes need to know the current position of the pointer on the screen − even when GDI is simulating the pointer (such that the driver no longer gets normal <b>DrvMovePointer</b> calls) − in order to handle panning virtual displays. To receive this notification, the driver should set the GCAPS_PANNING flag in the <b>flGraphicsCaps</b> field of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

<b>DrvMovePointer</b> will not be called while any thread is drawing in the display driver unless the GCAPS_ASYNCMOVE flag is set in the <b>flGraphicsCaps</b> member of DEVINFO.

<b>DrvMovePointer</b> must be implemented in display drivers only when <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpointershape">DrvSetPointerShape</a> is also implemented.

If a driver has registered the specified pointer using <a href="/windows/desktop/api/winddi/nf-winddi-drvsetpointershape">DrvSetPointerShape</a>, <b>DrvMovePointer</b> must not fail.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsetpointershape">DrvSetPointerShape</a>



<a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a>