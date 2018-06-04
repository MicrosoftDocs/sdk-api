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

If the physical device is palette-managed, GDI will call <a href="https://msdn.microsoft.com/library/windows/hardware/ff556282">DrvSetPalette</a> to reset the device's palette. The driver does not then need to keep track of the current pointer state because Window Manager selects the correct pointer shape and moves it to the current position. The console manager ensures that desktops are properly redrawn.

<b>DrvAssertMode</b> must be implemented in display drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556233">DrvGetModes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556282">DrvSetPalette</a>
 

 

