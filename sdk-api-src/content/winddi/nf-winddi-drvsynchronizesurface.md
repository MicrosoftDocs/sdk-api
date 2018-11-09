---
UID: NF:winddi.DrvSynchronizeSurface
title: DrvSynchronizeSurface function
author: windows-sdk-content
description: The DrvSynchronizeSurface function informs the driver that GDI needs to write to the specified surface. This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.
old-location: display\drvsynchronizesurface.htm
tech.root: display
ms.assetid: 717e0738-71a0-45e1-a479-337fab2998ab
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DrvSynchronizeSurface, DrvSynchronizeSurface function [Display Devices], ddifncs_ab69a2cb-5b19-4a94-a78e-2c21d2950ff8.xml, display.drvsynchronizesurface, winddi/DrvSynchronizeSurface
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
 - DrvSynchronizeSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvSynchronizeSurface function


## -description


The <b>DrvSynchronizeSurface</b> function informs the driver that GDI needs to write to the specified surface. This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that identifies the surface on which the drawing synchronization is to occur.


### -param prcl

Specifies a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that represents the surface that GDI will draw into, or <b>NULL</b>. If this does not collide with the drawing operation in progress, the driver can elect to let GDI draw without waiting for the coprocessor to complete.


### -param fl

Is a flag that specifies the event for which GDI is making the synchronization request. This parameter can be one of the following values:





#### DSS_TIMER_EVENT

GDI is calling this function due to a synchronization timer event. Timer events are generated for only those drivers that specify the GCAPS2_SYNCTIMER bit of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure.



#### DSS_FLUSH_EVENT

GDI is calling this function due to a synchronization flush event. These flush events are generated for only those drivers that specify the GCAPS2_SYNCFLUSH bit of the <a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a> structure.


## -returns



None




## -remarks



This function allows drawing operations performed by a device's coprocessor to be coordinated with GDI.

<b>DrvSynchronizeSurface</b> can be optionally implemented in display drivers. GDI calls this function only if it is hooked by <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>. GDI calls <b>DrvSynchronizeSurface</b> just before drawing directly onto the device surface.

<b>DrvSynchronizeSurface</b> is intended to support devices that use a coprocessor for drawing. Such a device can start a long drawing operation and return to GDI while the operation continues. If the device driver does not perform all drawing operations to the surface, it is possible that a subsequent drawing operation will be handled by GDI. In this case, it is necessary for GDI to wait for the coprocessor to complete its work before GDI can draw on the surface.

This function should return when it is safe for GDI to draw on the surface within the rectangular region specified by <i>prcl</i>.

<b>DrvSynchronizeSurface</b> is not itself an output function.




## -see-also




<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/ed9b7db3-1409-4aa6-9ee1-9ece53e747a6">DrvSynchronize</a>



<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>
 

 

