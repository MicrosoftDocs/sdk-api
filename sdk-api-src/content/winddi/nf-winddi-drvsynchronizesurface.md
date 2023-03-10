---
UID: NF:winddi.DrvSynchronizeSurface
title: DrvSynchronizeSurface function (winddi.h)
description: The DrvSynchronizeSurface function informs the driver that GDI needs to write to the specified surface. This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.
helpviewer_keywords: ["DrvSynchronizeSurface","DrvSynchronizeSurface function [Display Devices]","ddifncs_ab69a2cb-5b19-4a94-a78e-2c21d2950ff8.xml","display.drvsynchronizesurface","winddi/DrvSynchronizeSurface"]
old-location: display\drvsynchronizesurface.htm
tech.root: display
ms.assetid: 717e0738-71a0-45e1-a479-337fab2998ab
ms.date: 12/05/2018
ms.keywords: DrvSynchronizeSurface, DrvSynchronizeSurface function [Display Devices], ddifncs_ab69a2cb-5b19-4a94-a78e-2c21d2950ff8.xml, display.drvsynchronizesurface, winddi/DrvSynchronizeSurface
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
 - DrvSynchronizeSurface
 - winddi/DrvSynchronizeSurface
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
 - DrvSynchronizeSurface
---

# DrvSynchronizeSurface function


## -description

The <b>DrvSynchronizeSurface</b> function informs the driver that GDI needs to write to the specified surface. This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.

## -parameters

### -param pso

Pointer to a <a href="/windows/desktop/api/winddi/ns-winddi-surfobj">SURFOBJ</a> structure that identifies the surface on which the drawing synchronization is to occur.

### -param prcl

Specifies a <a href="/windows/desktop/api/windef/ns-windef-rectl">RECTL</a> structure that represents the surface that GDI will draw into, or <b>NULL</b>. If this does not collide with the drawing operation in progress, the driver can elect to let GDI draw without waiting for the coprocessor to complete.

### -param fl

Is a flag that specifies the event for which GDI is making the synchronization request. This parameter can be one of the following values:





#### DSS_TIMER_EVENT

GDI is calling this function due to a synchronization timer event. Timer events are generated for only those drivers that specify the GCAPS2_SYNCTIMER bit of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.



#### DSS_FLUSH_EVENT

GDI is calling this function due to a synchronization flush event. These flush events are generated for only those drivers that specify the GCAPS2_SYNCFLUSH bit of the <a href="/windows/desktop/api/winddi/ns-winddi-devinfo">DEVINFO</a> structure.

## -remarks

This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.

<b>DrvSynchronizeSurface</b> can be optionally implemented in display drivers. GDI calls this function only if it is hooked by <a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>. GDI calls <b>DrvSynchronizeSurface</b> just before drawing directly onto the device surface.

<b>DrvSynchronizeSurface</b> is intended to support devices that use a coprocessor for drawing. Such a device can start a long drawing operation and return to GDI while the operation continues. If the device driver does not perform all drawing operations to the surface, it is possible that a subsequent drawing operation will be handled by GDI. In this case, it is necessary for GDI to wait for the coprocessor to complete its work before GDI can draw on the surface.

This function should return when it is safe for GDI to draw on the surface within the rectangular region specified by <i>prcl</i>.

<b>DrvSynchronizeSurface</b> is not itself an output function.

## -see-also

<a href="/windows/desktop/api/winddi/nf-winddi-drvenablepdev">DrvEnablePDEV</a>



<a href="/windows/desktop/api/winddi/nf-winddi-drvsynchronize">DrvSynchronize</a>



<a href="/windows/desktop/api/winddi/nf-winddi-engassociatesurface">EngAssociateSurface</a>