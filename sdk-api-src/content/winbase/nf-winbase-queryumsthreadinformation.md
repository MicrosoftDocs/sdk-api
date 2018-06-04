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

# QueryUmsThreadInformation function


## -description


Retrieves information about the specified user-mode scheduling (UMS) worker thread.


## -parameters




### -param UmsThread [in]

A pointer to a UMS thread context. 


### -param UmsThreadInfoClass [in]

A <a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a> value that specifies the kind of information to retrieve. 


### -param UmsThreadInformation [out]

A pointer to a buffer to receive the specified information. The required size of this buffer depends on the specified information class.

If the information class is <b>UmsThreadContext</b> or <b>UmsThreadTeb</b>, the buffer must be <code>sizeof(PVOID)</code>.

If the information class is <b>UmsThreadIsSuspended</b> or <b>UmsThreadIsTerminated</b>, the buffer must be <code>sizeof(BOOLEAN)</code>.


### -param UmsThreadInformationLength [in]

The size of the <i>UmsThreadInformation</i> buffer, in bytes. 


### -param ReturnLength [out, optional]

A pointer to a ULONG variable. On output, this parameter receives the number of bytes written to the <i>UmsThreadInformation</i> buffer.


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
The buffer is too small for the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_INFO_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The specified information class is not supported.

</td>
</tr>
</table>
 




## -remarks



The <b>QueryUmsThreadInformation</b> function retrieves information about the specified UMS worker thread such as its application-defined context, its thread execution block (<a href="https://msdn.microsoft.com/fc77fc09-6319-4daa-ac96-1ded661ef800">TEB</a>), and whether the thread is suspended or terminated. 

The underlying structures for UMS worker threads are managed by the system. Information that is not exposed through <b>QueryUmsThreadInformation</b> should be considered reserved.




## -see-also




<a href="https://msdn.microsoft.com/19f190fd-1f78-4bb6-93eb-73a5c522b44d">SetUmsThreadInformation</a>



<a href="https://msdn.microsoft.com/2d6730b2-4d01-45f5-9514-0d91806f50d5">UMS_THREAD_INFO_CLASS</a>
 

 

