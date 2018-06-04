---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DrvSynchronize function


## -description


The <b>DrvSynchronize</b> function informs the driver that GDI needs to access a device-managed surface. This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> structure that identifies the device to be synchronized with GDI. This parameter is the device handle returned to GDI by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


### -param prcl

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569236">RECTL</a> structure. This parameter should be ignored by the driver.


## -returns



None




## -remarks



This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.

<b>DrvSynchronize</b> can be optionally implemented in display drivers. GDI calls this function only if it is hooked by <a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>. GDI calls <b>DrvSynchronize</b> just before drawing directly onto the device surface. GDI will call <a href="https://msdn.microsoft.com/library/windows/hardware/ff557273">DrvSynchronizeSurface</a> instead of <b>DrvSynchronize</b> in drivers that implement both of these functions.

This function should return only when it is safe for GDI to access any device-managed surface. That is, <b>DrvSynchronize</b> should delay returning from the call until all asynchronous drawing operations have been completed by the device's coprocessor, thus indicating that it is safe for GDI to access any device-managed surface.

<b>DrvSynchronize</b> is intended to support devices that use a coprocessor for drawing. Such a device can treat some drawing operations as asynchronous, returning to GDI from the operation before the drawing is complete. If this is the case, it is possible that a subsequent drawing operation will be handled by GDI. In order for GDI to safely access device-managed surfaces, it must have a means of ensuring that any <a href="https://msdn.microsoft.com/4ef14b5b-128b-4b7c-9211-116e8bd60cab">asynchronous rendering</a> being done by the device's coprocessor is complete. By calling this function, GDI synchronizes access to a device-managed surface with the driver.

GDI will never call <b>DrvSynchronize</b> for device-managed surfaces. <b>DrvSynchronize</b> is not itself an output function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557273">DrvSynchronizeSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564183">EngAssociateSurface</a>
 

 

