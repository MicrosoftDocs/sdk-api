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

# RtlCharToInteger function


## -description


Converts a character string to an integer.


## -parameters




### -param String [in]

A pointer to the string to convert. The format of the string is as follows: 

[whitespace] [{+ | -}] [0 [{x | o | b}]] [digits]


### -param Base [in, optional]

<b>ULONG</b> that contains the number base to use for the conversion, such as base 10. Only base 2, 8, 10, and 16 are supported.


### -param Value [out]

A pointer to a <b>ULONG</b> that receives the integer that resulted from the conversion.


## -returns



If the function succeeds, the function returns <b>STATUS_SUCCESS</b>.




## -remarks



When converting strings to integers the preferred function to use is <a href="1787c96a-f283-4a83-9325-33cfc1c7e240">strtol, wcstol</a>.

There is no import library for this function. Use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> rather than linking to the function directly.



