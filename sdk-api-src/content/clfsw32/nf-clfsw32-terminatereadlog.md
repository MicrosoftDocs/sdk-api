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

# TerminateReadLog function


## -description


Terminates a read context. This function frees system-allocated resources associated with the specified read context. Do not attempt to read log records after calling this function; you will receive indeterminate results.




## -parameters




### -param pvCursorContext [in]

A pointer to a  read context that is returned by <a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a> or <a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>.  


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following  list identifies the possible error codes:




## -remarks




        It is important to deallocate unused read contexts.  Failure to call this function causes resource leaks.




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/1c56c47b-d898-4c70-ba70-8978057c66b9">ReadLogRecord</a>



<a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>
 

 

