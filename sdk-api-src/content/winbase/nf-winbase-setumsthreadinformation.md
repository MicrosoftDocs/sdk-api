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

# SetUmsThreadInformation function


## -description


Sets application-specific context information for the specified user-mode scheduling (UMS) worker thread.


## -parameters




### -param UmsThread [in]

A pointer to a UMS thread context. 


### -param UmsThreadInfoClass [in]

A <a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a> value that specifies the kind of information to set. This parameter must be <b>UmsThreadUserContext</b>.


### -param UmsThreadInformation [in]

A pointer to a buffer that contains the information to set.


### -param UmsThreadInformationLength [in]

The size of the <i>UmsThreadInformation</i> buffer, in bytes. 


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INFO_LENGTH_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The buffer size does not match the  required size for the specified information class. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The <i>UmsThreadInfoClass</i> parameter specifies an information class that is not supported.

</td>
</tr>
</table>
 




## -remarks



The <b>SetUmsThreadInformation</b> function can be used to set an application-defined context for the specified UMS worker thread. The context information can consist of anything the application might find useful to track, such as per-scheduler or per-worker thread state. The underlying structures for UMS worker threads are managed by the system and should not be modified directly. 

The <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> function can be used to retrieve other exposed information about the specified thread, such as its thread execution block (<a href="https://msdn.microsoft.com/fc77fc09-6319-4daa-ac96-1ded661ef800">TEB</a>) and whether the thread is suspended or terminated. Information that is not exposed through <b>QueryUmsThreadInformation</b> should be considered reserved.




## -see-also




<a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a>
 

 

