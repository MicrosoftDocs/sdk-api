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

# DeleteLogFile function


## -description


Marks a log for deletion. The log is actually deleted when all handles, marshaling areas, and read contexts to the log are closed.  If the log is a physical log, its underlying containers are deleted.

When a log is marked for deletion, requests to open new client log streams fail. <div class="alert"><b>Note</b>  A closely related function is <a href="https://msdn.microsoft.com/2426058f-312c-4946-ac12-52e55a3307b5">DeleteLogByHandle</a>, which deletes a log when given the handle of the file.</div>
<div> </div>



## -parameters




### -param pszLogFileName [in]

The name of the log. 

This  name is specified when creating the log  by using  <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>. The following example identifies the format  to use:

<b>log:&lt;</b><i>log name</i><b>&gt;[::&lt;</b><i>log stream name</i><b>&gt;]</b>

&lt;<i>log  name</i>&gt; corresponds to a valid file path in the  file system.

&lt;<i>log stream name</i>&gt; is the unique name of a log stream in the log.

  For more information, see <a href="https://msdn.microsoft.com/a7099979-346c-434d-8af1-6bf1d5a0512f">Log Types</a>.


### -param OPTIONAL

TBD




#### - pvReserved [in, optional]

This parameter is reserved and should be set to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/2426058f-312c-4946-ac12-52e55a3307b5">DeleteLogByHandle</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

