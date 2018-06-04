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

# FLOATOBJ_GreaterThan function


## -description


The <b>FLOATOBJ_GreaterThan</b> function determines whether the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a> is greater than the second FLOATOBJ.


## -parameters




### -param

TBD




#### - pf [in]

Pointer to the first FLOATOBJ.


#### - pf1 [in]

Pointer to the second FLOATOBJ.


## -returns



<b>FLOATOBJ_GreaterThan </b>returns <b>TRUE</b> if *<i>pf</i> is greater than *<i>pf1</i>; otherwise it returns <b>FALSE</b>.




## -remarks



The FLOATOBJ<b>_</b><i>Xxx</i> services allow graphics drivers to emulate floating-point arithmetic. An NT-based operating system does not support kernel-mode floating-point operations on some systems.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565804">FLOATOBJ</a>
 

 

