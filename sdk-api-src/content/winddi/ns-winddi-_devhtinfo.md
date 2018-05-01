---
UID: NS:winddi._DEVHTINFO
title: "_DEVHTINFO"
author: windows-driver-content
description: The DEVHTINFO structure is used as input to the HTUI_DeviceColorAdjustment function.
old-location: display\devhtinfo.htm
old-project: display
ms.assetid: 81abebbf-97f2-422f-b0ab-f6f920e09fef
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: "*PDEVHTINFO, DEVHTINFO, DEVHTINFO structure [Display Devices], PDEVHTINFO, PDEVHTINFO structure pointer [Display Devices], _DEVHTINFO, display.devhtinfo, grstrcts_9ec57bb2-b77e-419b-8d26-03db8485cf35.xml, winddi/DEVHTINFO, winddi/PDEVHTINFO"
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
req.typenames: DEVHTINFO, *PDEVHTINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winddi.h
api_name:
-	DEVHTINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DEVHTINFO structure


## -description


The DEVHTINFO structure is used as input to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567308">HTUI_DeviceColorAdjustment</a> function.


## -struct-fields




### -field HTFlags

Is a set of caller-supplied flags indicating halftone attributes. See the <b>flHTFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a> structure for a complete list of possible values.


### -field HTPatternSize

Is a caller-supplied value that must be one of the HTPAT_SIZE-prefixed constants defined in <i>winddi.h</i>.


### -field DevPelsDPI

For printers, specifies the number of dots per inch. See the description of the <b>ulDevicePelsDPI</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a> structure for more information.

For displays, this member should be set to zero.


### -field ColorInfo

Is a caller-supplied pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff539441">COLORINFO</a> structure containing halftoning color information.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539441">COLORINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566484">GDIINFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff567308">HTUI_DeviceColorAdjustment</a>
 

 

