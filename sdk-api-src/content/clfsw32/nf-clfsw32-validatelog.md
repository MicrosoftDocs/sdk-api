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

# ValidateLog function


## -description


Validates the consistency of   the log metadata and data before log archive and after log restore.


## -parameters




### -param pszLogFileName [in]

The name of the log. 

The  name is specified when creating the log  by using  <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>. The following example identifies the format  to use:

<i>Log</i><b>:&lt;</b><i>LogName</i><b>&gt;[::&lt;</b><i>LogStreamName</i><b>&gt;]</b>

<b>&lt;</b><i>LogName</i><b>&gt;</b> corresponds to a valid file path  in  the   file system.

<b>&lt;</b><i>LogStreamName</i><b>&gt;</b> is  the unique name of a log stream in the dedicated log.   

For more information, see <a href="https://msdn.microsoft.com/a7099979-346c-434d-8af1-6bf1d5a0512f">Log Types</a>.


### -param OPTIONAL

TBD


### -param pcbBuffer [in, out]

A pointer to a variable that, on input, specifies the size of the <i>pinfoBuffer</i> metadata buffer, in bytes.  

On output, it receives the amount of information that is copied to the buffer, in bytes.


#### - pinfoBuffer [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541790">CLFS_INFORMATION</a> structure that receives log metadata. 


#### - psaLogFile [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that  specifies the security attributes of a log. 

This parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

The following list identifies the  possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/06f5919e-b98f-4502-9653-9ef42c1ebe5a">
        CLFS_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

