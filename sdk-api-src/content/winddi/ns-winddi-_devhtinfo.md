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
 

 

