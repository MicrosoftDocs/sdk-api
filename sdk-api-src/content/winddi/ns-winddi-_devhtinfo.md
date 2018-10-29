---
UID: NS:winddi._DEVHTINFO
title: "_DEVHTINFO"
author: windows-sdk-content
description: The DEVHTINFO structure is used as input to the HTUI_DeviceColorAdjustment function.
old-location: display\devhtinfo.htm
tech.root: display
ms.assetid: 81abebbf-97f2-422f-b0ab-f6f920e09fef
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PDEVHTINFO, DEVHTINFO, DEVHTINFO structure [Display Devices], PDEVHTINFO, PDEVHTINFO structure pointer [Display Devices], _DEVHTINFO, display.devhtinfo, grstrcts_9ec57bb2-b77e-419b-8d26-03db8485cf35.xml, winddi/DEVHTINFO, winddi/PDEVHTINFO"
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
 - DEVHTINFO
product: Windows
targetos: Windows
req.typenames: DEVHTINFO, *PDEVHTINFO
req.redist: 
---

# _DEVHTINFO structure


## -description


The DEVHTINFO structure is used as input to the <a href="https://msdn.microsoft.com/063320e3-b103-4c9a-ae82-790e5b768dc9">HTUI_DeviceColorAdjustment</a> function.


## -struct-fields




### -field HTFlags

Is a set of caller-supplied flags indicating halftone attributes. See the <b>flHTFlags</b> member of the <a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a> structure for a complete list of possible values.


### -field HTPatternSize

Is a caller-supplied value that must be one of the HTPAT_SIZE-prefixed constants defined in <i>winddi.h</i>.


### -field DevPelsDPI

For printers, specifies the number of dots per inch. See the description of the <b>ulDevicePelsDPI</b> member of the <a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a> structure for more information.

For displays, this member should be set to zero.


### -field ColorInfo

Is a caller-supplied pointer to a <a href="https://msdn.microsoft.com/bbada28c-d855-4197-acf8-2a070423ddfe">COLORINFO</a> structure containing halftoning color information.


## -see-also




<a href="https://msdn.microsoft.com/bbada28c-d855-4197-acf8-2a070423ddfe">COLORINFO</a>



<a href="https://msdn.microsoft.com/f75f599f-43ea-4da6-a6e3-6591cf6d69f1">GDIINFO</a>



<a href="https://msdn.microsoft.com/063320e3-b103-4c9a-ae82-790e5b768dc9">HTUI_DeviceColorAdjustment</a>
 

 

