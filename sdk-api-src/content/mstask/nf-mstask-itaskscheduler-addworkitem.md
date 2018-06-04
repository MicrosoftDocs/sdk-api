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

# ITaskScheduler::AddWorkItem


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>AddWorkItem</b> method adds a task to the schedule of tasks.


## -parameters




### -param pwszTaskName [in]

A null-terminated string that specifies the name of the task to add. The task name must conform to Windows NT file-naming conventions, but cannot include backslashes because nesting within the task folder object is not allowed.


### -param pWorkItem [in]

A pointer to the task to add to the schedule.


## -returns



The 
<b>AddWorkItem</b> method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A task with the specified name already exists. The actual return value is HRESULT_FROM_WIN32(ERROR_FILE_EXISTS).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
</table>
 




## -remarks



Task scheduler provides two methods for adding work items: 
<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">NewWorkItem</a> and 
<b>AddWorkItem</b>. Of these methods, each has its specific advantage. 
<b>AddWorkItem</b> prevents naming collisions, but it also requires two disk write operations per call. One write operation is performed when the call to 
<b>AddWorkItem</b> creates an empty work item object on the disk, followed by another write operation when <b>IPersistFile::Save</b> is called.


<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">NewWorkItem</a> does not prevent naming collisions, but it requires only one disk write operation when <b>IPersistFile::Save</b> is called. Although 
<b>NewWorkItem</b> is more efficient with disk write operations, the application runs the risk of having another application create a work item with the same name before the call to <b>IPersistFile::Save</b> is made.




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>



<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>



<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">ITaskScheduler::NewWorkItem</a>
 

 

