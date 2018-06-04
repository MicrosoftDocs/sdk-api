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

# IS_INTRESOURCE macro


## -description


Determines whether a value is an integer identifier for a resource. 


## -parameters




### -param _r

TBD






#### - p

The pointer to be tested whether it contains an integer resource identifier. 


## -remarks



This macro checks whether all bits except the least 16 bits are zero. When true, <i>p</i> is an integer identifier for a resource. Otherwise it is typically a pointer to a string.




## -see-also




<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources Overview</a>
 

 

