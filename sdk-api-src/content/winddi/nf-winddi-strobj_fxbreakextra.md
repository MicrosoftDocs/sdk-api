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

# STROBJ_fxBreakExtra function


## -description


The <b>STROBJ_fxBreakExtra</b> function retrieves the amount of extra space to be added to each space character in a string when displaying and/or printing justified text.


## -parameters




### -param pstro

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a> structure of the string to be displayed.


## -returns



<b>STROBJ_fxBreakExtra</b> returns the amount of extra space to add to each space character in the string. A return value of zero indicates that no extra space is added to space characters in a string.




## -remarks



The extra space value is specified in pixel coordinates.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff569738">STROBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569744">STROBJ_fxCharacterExtra</a>
 

 

