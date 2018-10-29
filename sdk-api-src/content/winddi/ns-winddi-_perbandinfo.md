---
UID: NS:winddi._PERBANDINFO
title: "_PERBANDINFO"
author: windows-sdk-content
description: The PERBANDINFO structure is used as input to a printer graphics DLL's DrvQueryPerBandInfo function.
old-location: display\perbandinfo.htm
tech.root: display
ms.assetid: ec02542f-68d1-4d05-a4d1-e475725997ad
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PPERBANDINFO, PERBANDINFO, PERBANDINFO structure [Display Devices], PPERBANDINFO, PPERBANDINFO structure pointer [Display Devices], _PERBANDINFO, display.perbandinfo, grstrcts_130088d9-975d-4b22-be85-90e129c64455.xml, winddi/PERBANDINFO, winddi/PPERBANDINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Windows
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
 - PERBANDINFO
product: Windows
targetos: Windows
req.typenames: PERBANDINFO, *PPERBANDINFO
req.redist: 
---

# _PERBANDINFO structure


## -description


The PERBANDINFO structure is used as input to a printer graphics DLL's <a href="https://msdn.microsoft.com/2e2c1aa7-9ba4-4bf9-acfb-43212d3d4899">DrvQueryPerBandInfo</a> function.


## -struct-fields




### -field bRepeatThisBand

If <b>TRUE</b>, GDI redraws the previous band. If <b>FALSE</b>, GDI draws the next band.


### -field szlBand

Specifies a SIZEL structure that contains the width and height, in pixels, of the rectangle in which GDI can draw the band. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/08d81096-069f-4554-9bb9-d4a37c0950ac">SIZE</a> structure.


### -field ulHorzRes

Specifies the horizontal resolution GDI should use when scaling the band.


### -field ulVertRes

Specifies the vertical resolution GDI should use when scaling the band.


## -remarks



If the result of <b>ulHorzRes</b> divided by <b>ulVertRes</b> is smaller than the result obtained by dividing the same members of the <a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a> structure, the band is rendered smaller by the graphics engine. If the values are the same, no scaling is done. The resultant scale factor obtained from this structure cannot be larger than the one stored in GDIINFO.

When the band is scaled, the graphics engine anchors the smaller band to the upper-left corner of the original band.




## -see-also




<a href="https://msdn.microsoft.com/2e2c1aa7-9ba4-4bf9-acfb-43212d3d4899">DrvQueryPerBandInfo</a>



<a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a>
 

 

