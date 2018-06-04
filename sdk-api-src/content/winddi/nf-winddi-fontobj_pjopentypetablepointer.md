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

# FONTOBJ_pjOpenTypeTablePointer function


## -description


The <b>FONTOBJ_pjOpenTypeTablePointer</b> function returns a pointer to a view of an OpenType table.


## -parameters




### -param pfo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a> that identifies the font whose OpenType table is being queried.


### -param ulTag

Identifies the font table whose pointer is to be returned.


### -param pcjTable

Pointer to the location in which GDI returns the size in bytes of the table being queried.


## -returns



<b>FONTOBJ_pjOpenTypeTablePointer</b> returns a pointer to a view of the OpenType table. A return value of <b>NULL</b> indicates that the requested table is not present in this font.




## -remarks



<b>FONTOBJ_pjOpenTypeTablePointer</b> can be called by printer drivers that can download OpenType fonts or parts of OpenType fonts to the printer.

The pointer to a table returned by <b>FONTOBJ_pjOpenTypeTablePointer</b> is guaranteed to be valid only during the scope of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a> call to which <i>pfo</i> is passed as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557277">DrvTextOut</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565974">FONTOBJ</a>
 

 

