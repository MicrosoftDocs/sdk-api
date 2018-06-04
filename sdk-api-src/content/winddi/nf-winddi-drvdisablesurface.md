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

# DrvDisableSurface function


## -description


The <b>DrvDisableSurface</b> function is used by GDI to notify a driver that the surface created by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a> for the current device is no longer needed.


## -parameters




### -param dhpdev

Handle to the physical device's <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a>. This is the handle to the device whose surface is to be released.


## -returns



None




## -remarks



The driver should free any memory and resources used by the surface associated with the PDEV as soon as the physical device is disabled.

If the driver has been disabled by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a>, the driver must not access the hardware during <b>DrvDisableSurface</b> because another active PDEV might be in use. Any necessary hardware changes should have been performed during the call to <b>DrvAssertMode</b>. A driver should keep track of whether it has been disabled by <b>DrvAssertMode</b> so that it can perform proper cleanup operations in <b>DrvDisableSurface</b>.

If the physical device has an enabled surface, GDI calls <b>DrvDisableSurface</b> before calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff556198">DrvDisablePDEV</a>.

<b>DrvDisableSurface</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556196">DrvDisableDriver</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556198">DrvDisablePDEV</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556214">DrvEnableSurface</a>
 

 

