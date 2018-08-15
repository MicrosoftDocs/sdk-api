---
UID: NF:winddi.DrvSynchronize
title: DrvSynchronize function
author: windows-sdk-content
description: The DrvSynchronize function informs the driver that GDI needs to access a device-managed surface. This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.
old-location: display\drvsynchronize.htm
old-project: display
ms.assetid: ed9b7db3-1409-4aa6-9ee1-9ece53e747a6
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DrvSynchronize, DrvSynchronize function [Display Devices], ddifncs_dadafaae-d13a-4a52-b179-a8b14a835a24.xml, display.drvsynchronize, winddi/DrvSynchronize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSynchronize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DrvSynchronize function


## -description


The <b>DrvSynchronize</b> function informs the driver that GDI needs to access a device-managed surface. This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> structure that identifies the device to be synchronized with GDI. This parameter is the device handle returned to GDI by <a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>.


### -param prcl

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure. This parameter should be ignored by the driver.


## -returns



None




## -remarks



This function allows asynchronous drawing operations performed by a device's coprocessor to be coordinated with GDI accesses.

<b>DrvSynchronize</b> can be optionally implemented in display drivers. GDI calls this function only if it is hooked by <a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>. GDI calls <b>DrvSynchronize</b> just before drawing directly onto the device surface. GDI will call <a href="https://msdn.microsoft.com/717e0738-71a0-45e1-a479-337fab2998ab">DrvSynchronizeSurface</a> instead of <b>DrvSynchronize</b> in drivers that implement both of these functions.

This function should return only when it is safe for GDI to access any device-managed surface. That is, <b>DrvSynchronize</b> should delay returning from the call until all asynchronous drawing operations have been completed by the device's coprocessor, thus indicating that it is safe for GDI to access any device-managed surface.

<b>DrvSynchronize</b> is intended to support devices that use a coprocessor for drawing. Such a device can treat some drawing operations as asynchronous, returning to GDI from the operation before the drawing is complete. If this is the case, it is possible that a subsequent drawing operation will be handled by GDI. In order for GDI to safely access device-managed surfaces, it must have a means of ensuring that any <a href="https://msdn.microsoft.com/4ef14b5b-128b-4b7c-9211-116e8bd60cab">asynchronous rendering</a> being done by the device's coprocessor is complete. By calling this function, GDI synchronizes access to a device-managed surface with the driver.

GDI will never call <b>DrvSynchronize</b> for device-managed surfaces. <b>DrvSynchronize</b> is not itself an output function.




## -see-also




<a href="https://msdn.microsoft.com/9a7ed18a-f21c-486b-9261-59a3fe5aef9e">DrvEnablePDEV</a>



<a href="https://msdn.microsoft.com/717e0738-71a0-45e1-a479-337fab2998ab">DrvSynchronizeSurface</a>



<a href="https://msdn.microsoft.com/8cb6d4bf-67bd-4bfb-9605-eeb954fc590c">EngAssociateSurface</a>
 

 

