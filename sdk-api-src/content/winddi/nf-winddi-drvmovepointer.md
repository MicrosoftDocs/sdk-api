---
UID: NF:winddi.DrvMovePointer
title: DrvMovePointer function
author: windows-sdk-content
description: The DrvMovePointer function moves the pointer to a new position and ensures that GDI does not interfere with the display of the pointer.
old-location: display\drvmovepointer.htm
tech.root: display
ms.assetid: eb117f39-0823-4eb7-8628-fa4399a13ec6
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DrvMovePointer, DrvMovePointer function [Display Devices], ddifncs_4fda6dd1-abd6-45fa-ba92-d20352fe35c5.xml, display.drvmovepointer, winddi/DrvMovePointer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvMovePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvMovePointer function


## -description


The <b>DrvMovePointer</b> function moves the pointer to a new position and ensures that GDI does not interfere with the display of the pointer.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface of a display device.


### -param x [in]

Specify the <i>x</i> coordinate on the display where the driver should position the hot spot of the pointer.

A negative <i>x</i> value indicates that the driver should remove the pointer from the display because drawing is about to occur where it is presently located. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the driver should restore the pointer.


### -param y [in]

Specify the <i>y</i> coordinate on the display where the driver should position the hot spot of the pointer.

When the driver has set the GCAPS_PANNING flag in the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure, a negative <i>y</i> value indicates that GDI is calling this function only to notify the driver of the cursor's current position. The current position can be computed as (<i>x</i>, <i>y</i>+<i>pso</i>-&gt;sizlBitmap.cy). A driver that does not set the GCAPS_PANNING flag will never receive a negative <i>y</i> coordinate.


### -param prcl [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.


## -returns



None




## -remarks



Drivers sometimes need to know the current position of the pointer on the screen − even when GDI is simulating the pointer (such that the driver no longer gets normal <b>DrvMovePointer</b> calls) − in order to handle panning virtual displays. To receive this notification, the driver should set the GCAPS_PANNING flag in the <b>flGraphicsCaps</b> field of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure.

<b>DrvMovePointer</b> will not be called while any thread is drawing in the display driver unless the GCAPS_ASYNCMOVE flag is set in the <b>flGraphicsCaps</b> member of DEVINFO.

<b>DrvMovePointer</b> must be implemented in display drivers only when <a href="https://msdn.microsoft.com/3cc186df-572b-48ed-ac0b-56c8d91a9794">DrvSetPointerShape</a> is also implemented.

If a driver has registered the specified pointer using <a href="https://msdn.microsoft.com/3cc186df-572b-48ed-ac0b-56c8d91a9794">DrvSetPointerShape</a>, <b>DrvMovePointer</b> must not fail.




## -see-also




<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/3cc186df-572b-48ed-ac0b-56c8d91a9794">DrvSetPointerShape</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

