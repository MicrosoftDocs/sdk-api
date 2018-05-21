---
UID: NS:winddi._PERBANDINFO
title: "_PERBANDINFO"
author: windows-driver-content
description: The PERBANDINFO structure is used as input to a printer graphics DLL's DrvQueryPerBandInfo function.
old-location: display\perbandinfo.htm
old-project: display
ms.assetid: ec02542f-68d1-4d05-a4d1-e475725997ad
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: "*PPERBANDINFO, PERBANDINFO, PERBANDINFO structure [Display Devices], PPERBANDINFO, PPERBANDINFO structure pointer [Display Devices], _PERBANDINFO, display.perbandinfo, grstrcts_130088d9-975d-4b22-be85-90e129c64455.xml, winddi/PERBANDINFO, winddi/PPERBANDINFO"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PERBANDINFO, *PPERBANDINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	PERBANDINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _PERBANDINFO structure


## -description


The PERBANDINFO structure is used as input to a printer graphics DLL's <a href="https://msdn.microsoft.com/library/windows/hardware/ff556268">DrvQueryPerBandInfo</a> function.


## -struct-fields




### -field bRepeatThisBand

If <b>TRUE</b>, GDI redraws the previous band. If <b>FALSE</b>, GDI draws the next band.


### -field szlBand

Specifies a SIZEL structure that contains the width and height, in pixels, of the rectangle in which GDI can draw the band. A SIZEL structure is identical to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure.


### -field ulHorzRes

Specifies the horizontal resolution GDI should use when scaling the band.


### -field ulVertRes

Specifies the vertical resolution GDI should use when scaling the band.


## -remarks



If the result of <b>ulHorzRes</b> divided by <b>ulVertRes</b> is smaller than the result obtained by dividing the same members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a> structure, the band is rendered smaller by the graphics engine. If the values are the same, no scaling is done. The resultant scale factor obtained from this structure cannot be larger than the one stored in GDIINFO.

When the band is scaled, the graphics engine anchors the smaller band to the upper-left corner of the original band.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556268">DrvQueryPerBandInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a>
 

 

