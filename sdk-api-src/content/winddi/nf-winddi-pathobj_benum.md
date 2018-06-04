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

# PATHOBJ_bEnum function


## -description


The <b>PATHOBJ_bEnum</b> function retrieves the next PATHDATA record from a specified path and enumerates the curves in the path.


## -parameters




### -param ppo

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a> structure whose curves and/or lines are to be enumerated.


### -param ppd

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PATHDATA</a> structure that is to be filled.


## -returns



The return value is <b>TRUE</b> if the specified path contains more PATHDATA records, indicating that this service should be called again. Otherwise, if the output is the last PATHDATA record in the path, the return value is <b>FALSE</b>.




## -remarks



<b>PATHOBJ_bEnum</b> can be called only after a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff568856">PATHOBJ_vEnumStart</a> has been made.

A PATHDATA structure describes all or part of a subpath (a connected part of a path). For example, a <b>MoveTo</b> call by the application within a path begins a new subpath.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff568848">PATHDATA</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568849">PATHOBJ</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568856">PATHOBJ_vEnumStart</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568857">PATHOBJ_vEnumStartClipLines</a>
 

 

