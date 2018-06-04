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

# ITaskService::GetRunningTasks


## -description


Gets a collection of running tasks.<div class="alert"><b>Note</b>  <b>ITaskService::GetRunningTasks</b> will only return a collection of running tasks that are running at or below a user's security context. For example, for members of the Administrators group, <b>GetRunningTasks</b> will return a collection of all running tasks, but for members of the Users group, <b>GetRunningTasks</b> will only return a collection of tasks running under the Users group security context.</div>
<div> </div>



## -parameters




### -param flags [in]

A value from the <a href="https://msdn.microsoft.com/c77e597b-c8d9-426c-aa9d-7bb8536b349a">TASK_ENUM_FLAGS</a> enumeration. Pass in 0 to return a collection of running tasks that are not hidden tasks.


### -param ppRunningTasks






#### - retVal [out]

An <a href="https://msdn.microsoft.com/f95efba5-563d-49c0-81d3-143aa158ad8f">IRunningTaskCollection</a> interface that contains the currently running tasks.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/f95efba5-563d-49c0-81d3-143aa158ad8f">IRunningTaskCollection</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



This method can return one of these values.

<table>
<tr>
<th></th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument was specified in the method call. Passing a nonzero value to the <i>flags</i> parameter will return <b>E_INVALIDARG</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed into the <i>retVal</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ONLY_IF_CONNECTED)</b></dt>
</dl>
</td>
<td width="60%">
The user has not connected to the service.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f95efba5-563d-49c0-81d3-143aa158ad8f">IRunningTaskCollection</a>



<a href="https://msdn.microsoft.com/2459aaae-4c3a-458a-ad2c-bfff3a0322d3">ITaskService</a>



<a href="https://msdn.microsoft.com/c77e597b-c8d9-426c-aa9d-7bb8536b349a">TASK_ENUM_FLAGS</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

