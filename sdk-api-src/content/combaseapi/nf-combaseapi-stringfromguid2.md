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

# StringFromGUID2 function


## -description


Converts a globally unique identifier (GUID) into a string of printable characters.




## -parameters




### -param rguid [in]

The GUID to be converted.


### -param lpsz [out]

 A pointer to a caller-allocated string variable to receive the resulting string. The string that represents <i>rguid</i> includes enclosing braces.


### -param cchMax [in]

The number of characters available in the <i>lpsz</i> buffer.



## -returns



If the function succeeds, the return value is the number of characters in the returned string, including the null terminator. If the buffer is too small to contain the string, the return value is 0.




## -see-also




<a href="https://msdn.microsoft.com/61210ebd-cbf3-4e78-b077-53d2779053eb">StringFromCLSID</a>
 

 

