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

# DrvDisablePDEV function


## -description


The <b>DrvDisablePDEV</b> function is used by GDI to notify a driver that the specified <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> is no longer needed.


## -parameters




### -param dhpdev

Handle to the <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> of the physical device to be disabled. This value is the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>.


## -returns



None




## -remarks



If the physical device has an enabled surface, GDI calls <b>DrvDisablePDEV</b> after calling <a href="https://msdn.microsoft.com/library/windows/hardware/ff556200">DrvDisableSurface</a>. The driver should free any memory and resources used by the PDEV.

<b>DrvDisablePDEV</b> is required for graphics drivers.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556178">DrvAssertMode</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556200">DrvDisableSurface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556211">DrvEnablePDEV</a>
 

 

