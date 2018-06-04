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

# SysStringLen function


## -description


Returns the length of a BSTR.


## -parameters




### -param pbstr

TBD




#### - bstr [in, optional]

A previously allocated string.


## -returns



The number of characters in <i>bstr</i>, not including the terminating null character. If <i>bstr</i> is null the return value is zero.




## -remarks



The returned value may be different from <b>strlen</b>(bstr) if the BSTR contains embedded Null characters. This function always returns the number of characters specified in the cch parameter of the <a href="F98BFF39-BC5F-4A81-85D7-D5228E20FBC8">SysAllocStringLen</a> function used to allocate the BSTR.




## -see-also




<a href="https://msdn.microsoft.com/323cefbf-836c-4c9d-bcbe-f2663a57d2b5">String Manipulation Functions</a>
 

 

