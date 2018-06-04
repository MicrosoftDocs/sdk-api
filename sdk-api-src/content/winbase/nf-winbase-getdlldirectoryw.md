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

# GetDllDirectoryW function


## -description


Retrieves the application-specific portion of the search path used to locate DLLs for the 
   application.


## -parameters




### -param nBufferLength [in]

The size of the output buffer, in characters.


### -param lpBuffer [out]

A pointer to a buffer that receives the application-specific portion of the search path.


## -returns



If the function succeeds, the return value is the length of the string copied to 
       <i>lpBuffer</i>, in characters, not including the terminating null character. If the return 
       value is greater than <i>nBufferLength</i>, it specifies the size of the buffer required for 
       the path.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0502 
    or later. For more information, see 
    <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>



<a href="https://msdn.microsoft.com/c0c57554-3d98-487c-8bae-c594620d5a00">SetDllDirectory</a>
 

 

