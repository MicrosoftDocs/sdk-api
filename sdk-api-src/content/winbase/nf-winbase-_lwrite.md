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

# _lwrite function


## -description


<p class="CCE_Message">[This function is provided for compatibility with 16-bit versions of Windows. New applications should use the <b>WriteFile</b> function.]

Writes data to the specified file.


## -parameters




### -param hFile

A handle to the file that receives the data. This handle is created by <a href="https://msdn.microsoft.com/89e19823-c720-4bfc-95d5-18942573dd94">_lcreat</a>.


### -param lpBuffer

The buffer that contains the data to be added.


### -param uBytes

TBD




#### - cbWrite

The number of bytes to write to the file.


## -returns



If the function succeeds, the return value is the number of bytes written to the file. Otherwise, the return value is HFILE_ERROR. To get extended error information, use the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

