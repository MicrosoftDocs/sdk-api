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

# PALOBJ_cGetColors function


## -description


The <b>PALOBJ_cGetColors</b> function copies RGB colors from an indexed palette.


## -parameters




### -param ppalo

Pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff568844">PALOBJ</a> structure that contains the RGB colors to be copied.


### -param iStart

Specifies the starting color index.


### -param cColors

Specifies the number of colors to be written.


### -param pulColors

Pointer to the buffer in which the colors are to be written.


## -returns



The return value is the number of colors written if the function is successful. Otherwise, it is zero.




## -remarks



A graphics driver can call this function in its implementation of <a href="https://msdn.microsoft.com/library/windows/hardware/ff556282">DrvSetPalette</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556282">DrvSetPalette</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568844">PALOBJ</a>
 

 

