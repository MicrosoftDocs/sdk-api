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

# PDD_GETSCANLINE callback function


## -description


The <i>DdGetScanLine</i> callback function returns the number of the current physical scan line.


## -parameters




### -param Arg1








#### - pGetScanLine

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551591">DD_GETSCANLINEDATA</a> structure in which the driver returns the number of the current scan line.


## -returns



<i>DdGetScanLine</i> returns one of the following callback codes:




## -remarks



If the monitor is not in vertical blank, the driver should write the scan line value in the <b>dwScanLine</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551591">DD_GETSCANLINEDATA</a> structure at <i>pGetScanLine</i>. The number must be in the range [0, <i>n</i>], where scan line 0 is the first visible scan line and scan line <i>n</i> is the last visible scan line on the screen. The driver should then set DD_OK in the <b>ddRVal</b> member of <b>DD_GETSCANLINEDATA</b> and return DDHAL_DRIVER_HANDLED.

The scan line is indeterminate if a vertical blank is in progress. In this situation, the driver should set <b>ddRVal</b> to DDERR_VERTICALBLANKINPROGRESS and return DDHAL_DRIVER_HANDLED.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551591">DD_GETSCANLINEDATA</a>
 

 

