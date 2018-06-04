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

# PDD_SURFCB_BLT callback function


## -description


The <i>DdBlt</i> callback function performs a bit-block transfer.


## -parameters




### -param Arg1








#### - lpBlt

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550474">DD_BLTDATA</a> structure that contains the information required for the driver to perform the blit.


## -returns



<i>DdBlt</i> returns one of the following callback codes:




## -remarks



<i>DdBlt</i> can be optionally implemented in DirectDraw drivers.

Before performing the bit block transfer, the driver should ensure that a flip involving the destination surface is not in progress. If the destination surface is involved in a flip, the driver should set the <b>ddRVal</b> member of the DD_BLTDATA structure at <i>lpBlt</i> to DDERR_WASSTILLDRAWING and return DDHAL_DRIVER_HANDLED.

The driver should check <b>dwFlags</b> to determine the type of blit operation to perform. The driver should not check for flags that are undocumented.

When performing transparent (color keyed) blts, drivers should ignore any unused pixel bits in their comparisons. (For instance in 32bpp modes, the high byte is typically unused. This byte should not be used in the color key comparison.)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550474">DD_BLTDATA</a>
 

 

