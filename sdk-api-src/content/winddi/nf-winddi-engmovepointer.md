---
UID: NF:winddi.EngMovePointer
title: EngMovePointer function
author: windows-sdk-content
description: The EngMovePointer function moves the engine-managed pointer on the device.
old-location: display\engmovepointer.htm
tech.root: Display
ms.assetid: 6f427839-034e-46c3-a3b0-703a003af1e4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: EngMovePointer, EngMovePointer function [Display Devices], display.engmovepointer, gdifncs_2499e137-74e8-4624-8595-65d4fb489973.xml, winddi/EngMovePointer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngMovePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngMovePointer function


## -description


The <b>EngMovePointer</b> function moves the engine-managed pointer on the device.


## -parameters




### -param pso [in]

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the display device surface on which the pointer is to be moved.


### -param x [in]

Specify the x-coordinate on the display where the hot spot of the pointer should be positioned.

A negative <i>x</i> value indicates that the pointer should be removed from the display because drawing is about to occur at its present location. If the pointer has been removed from the display and the <i>x</i> value is nonnegative, the pointer should be restored.


### -param y [in]

Specify the y-coordinate on the display where the hot spot of the pointer should be positioned.


### -param prcl [in]

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure defining an area that bounds all pixels affected by the pointer on the display. The driver should pass the <i>prcl</i> parameter received by its <a href="https://msdn.microsoft.com/eb117f39-0823-4eb7-8628-fa4399a13ec6">DrvMovePointer</a> function. GDI will not draw in this rectangle without first removing the pointer from the screen. This parameter can be <b>NULL</b>.


## -returns



None




## -remarks



<b>EngMovePointer</b> must not be called while any thread is drawing in the display driver.




## -see-also




<a href="https://msdn.microsoft.com/5ba3e521-2e70-4a5b-979d-30a061275d42">DEVINFO</a>



<a href="https://msdn.microsoft.com/eb117f39-0823-4eb7-8628-fa4399a13ec6">DrvMovePointer</a>



<a href="https://msdn.microsoft.com/9b3a1e44-f3c6-4160-8d5d-d114511ad201">EngSetPointerShape</a>



<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

