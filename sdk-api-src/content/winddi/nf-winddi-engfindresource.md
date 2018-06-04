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

# EngFindResource function


## -description


The <b>EngFindResource</b> function determines the location of a resource in a module.


## -parameters




### -param h [in]

Handle to the module that contains the resource. This handle is obtained from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>.


### -param iName [in]

Is an integer identifier representing the name of the resource being looked up.


### -param iType [in]

Is an integer identifier representing the type of the resource being looked up.


### -param pulSize [out]

Pointer to a ULONG in which the resource's size, in bytes, is returned.


## -returns



The return value is a pointer to the address of the specified resource. The function returns <b>NULL</b> if an error occurs.




## -remarks



The size of a successfully located resource is returned in <i>pulSize</i>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a>
 

 

