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

# NtWaitForSingleObject function


## -description


Deprecated. Waits until the specified object attains a state of
    <code>signaled</code>. <b>NtWaitForSingleObject</b> is superseded by <a href="https://msdn.microsoft.com/e37ebff7-b44e-469d-81ab-7a6bd1a0c822">WaitForSingleObject</a>.


## -parameters




### -param Handle [in]

The handle to the wait object.


### -param Alertable [in]

Specifies whether an alert can be delivered when the object is waiting.



#### TRUE

The alert can be delivered.



#### FALSE

The alert cannot be delivered.


### -param OPTIONAL

TBD




#### - Timeout [in]

A pointer to an absolute or relative time over
        which the wait is to occur. Can be null. If a timeout is specified, and
    the object has not attained a state of <code>signaled</code> when the timeout
    expires, then the wait is automatically satisfied.  If an explicit
    timeout value of zero is specified, then no wait occurs if the
    wait cannot be satisfied immediately. 


## -returns



The wait completion status. The various NTSTATUS values are defined in NTSTATUS.H, which is distributed with the Windows DDK.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The specified
    object satisfied the wait. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
A
    timeout occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ALERTED</b></dt>
</dl>
</td>
<td width="60%">
The
    wait was aborted to deliver an alert to the current thread.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_USER_APC</b></dt>
</dl>
</td>
<td width="60%">
The wait was aborted to deliver a user <a href="_win32_Asynchronous_Procedure_Calls">Asynchronous Procedure Call (APC)</a> to the current thread.

</td>
</tr>
</table>
 




## -remarks



Because there is no import library for this function, you must use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a>.
		



