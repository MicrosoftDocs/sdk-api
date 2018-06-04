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

# STROBJ_fxCharacterExtra function


## -description


The <b>STROBJ_fxCharacterExtra</b> function retrieves the amount of extra space with which to augment each character's width in a string when displaying and/or printing it.


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure of the string to be displayed.


## -returns



<b>STROBJ_fxCharacterExtra</b> returns the amount of extra space to add to every character in the string. A return value of zero indicates that the string should be laid out using the characters' unaugmented widths.




## -remarks



The extra space value is specified in pixel coordinates.

<b>STROBJ_fxCharacterExtra</b> never fails.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569743">STROBJ_fxBreakExtra</a>
 

 

