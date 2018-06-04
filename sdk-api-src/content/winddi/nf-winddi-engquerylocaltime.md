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

# EngQueryLocalTime function


## -description


The <b>EngQueryLocalTime</b> function queries the local time.


## -parameters




### -param Arg1

TBD




#### - ptf [out]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff565470">ENG_TIME_FIELDS</a> structure that receives the local time.


## -returns



None




## -remarks



<b>EngQueryLocalTime</b> returns the time at the current locale in the ENG_TIME_FIELDS structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff565470">ENG_TIME_FIELDS</a>
 

 

