---
UID: NC:ddrawint.PDD_SURFCB_BLT
title: PDD_SURFCB_BLT
author: windows-sdk-content
description: The DdBlt callback function performs a bit-block transfer.
old-location: display\ddblt.htm
old-project: display
ms.assetid: 28e0c827-33f1-4b83-9f20-bbb66bc0e14a
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DdBlt, DdBlt callback function [Display Devices], PDD_SURFCB_BLT, PDD_SURFCB_BLT callback, ddfncs_464b3f37-739d-45c9-955d-3103c6a21047.xml, ddrawint/DdBlt, display.ddblt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
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
req.typenames: "*LPDDHAL_DESTROYDDLOCALDATA, DDHAL_DESTROYDDLOCALDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdBlt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PDD_SURFCB_BLT callback function


## -description


The <i>DdBlt</i> callback function performs a bit-block transfer.


## -parameters




### -param Arg1








#### - lpBlt

Points to the <a href="https://msdn.microsoft.com/e39bdfc4-89d0-4440-93d3-1b455cc9a8e5">DD_BLTDATA</a> structure that contains the information required for the driver to perform the blit.


## -returns



<i>DdBlt</i> returns one of the following callback codes:




## -remarks



<i>DdBlt</i> can be optionally implemented in DirectDraw drivers.

Before performing the bit block transfer, the driver should ensure that a flip involving the destination surface is not in progress. If the destination surface is involved in a flip, the driver should set the <b>ddRVal</b> member of the DD_BLTDATA structure at <i>lpBlt</i> to DDERR_WASSTILLDRAWING and return DDHAL_DRIVER_HANDLED.

The driver should check <b>dwFlags</b> to determine the type of blit operation to perform. The driver should not check for flags that are undocumented.

When performing transparent (color keyed) blts, drivers should ignore any unused pixel bits in their comparisons. (For instance in 32bpp modes, the high byte is typically unused. This byte should not be used in the color key comparison.)




## -see-also




<a href="https://msdn.microsoft.com/e39bdfc4-89d0-4440-93d3-1b455cc9a8e5">DD_BLTDATA</a>
 

 

