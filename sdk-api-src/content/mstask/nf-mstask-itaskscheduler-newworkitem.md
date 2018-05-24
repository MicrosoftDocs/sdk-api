---
UID: NF:mstask.ITaskScheduler.NewWorkItem
title: ITaskScheduler::NewWorkItem
author: windows-driver-content
description: The NewWorkItem method creates a new work item, allocating space for the work item and retrieving its address.
old-location: taskschd\itaskscheduler_newworkitem.htm
old-project: TaskSchd
ms.assetid: 1fbd65ae-0b54-4175-bf26-4226b1aabdc1
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ITaskScheduler interface [Task Scheduler],NewWorkItem method, ITaskScheduler.NewWorkItem, ITaskScheduler::NewWorkItem, NewWorkItem, NewWorkItem method [Task Scheduler], NewWorkItem method [Task Scheduler],ITaskScheduler interface, _msb_itaskscheduler_newworkitem, mstask/ITaskScheduler::NewWorkItem, taskschd.itaskscheduler_newworkitem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mstask.dll
api_name:
-	ITaskScheduler.NewWorkItem
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITaskScheduler::NewWorkItem


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>NewWorkItem</b> method creates a new <a href="w.htm">work item</a>, allocating space for the work item and retrieving its address.


## -parameters




### -param pwszTaskName [in]

A null-terminated string that specifies the name of the new work item. This name must conform to Windows NT file-naming conventions, but cannot include backslashes because nesting within the task folder object is not allowed.


### -param rclsid [in]

The class identifier of the work item to be created. The only class supported at this time, the task class, has the identifier CLSID_Ctask.


### -param riid [in]

The reference identifier of the interface being requested. The only interface supported at this time, 
<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>, has the identifier IID_ITask.


### -param ppUnk






#### - ppunk [out]

A pointer to an interface pointer that receives the requested interface. See Remarks for information on saving the work item to disk.


## -returns



The 
<b>NewWorkItem</b> method returns one of the following values.

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
A work item with the specified name already exists. The actual return value is HRESULT_FROM_WIN32 (ERROR_FILE_EXISTS).

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
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have permission to perform the operation. For more information, see <a href="https://msdn.microsoft.com/6ca182c3-eba8-43dd-bf2e-27dd972e3cf8">Scheduled Work Items</a>.

</td>
</tr>
</table>
 




## -remarks



This method handles memory allocation automatically when creating the new work item.

To save the work item to disk, call 
<a href="_com_ipersistfile_save">IPersistFile::Save</a> . This COM interface is supported by all work item interfaces (currently 
<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a> is the only supported work item interface).

Task scheduler provides two methods for adding work items: 
<b>NewWorkItem</b> and 
<a href="https://msdn.microsoft.com/5d776e19-c40e-4e0a-8ae1-a14c4f23b442">AddWorkItem</a>. Of these methods, each has its specific advantage. 
<b>AddWorkItem</b> prevents naming collisions, but also requires two disk write operations per call. One write operation is performed when the call to 
<b>AddWorkItem</b> creates an empty work item object on the disk, followed by another write operation when <a href="_com_ipersistfile_save">IPersistFile::Save</a> is called.

You can create a task by calling <a href="https://msdn.microsoft.com/5d776e19-c40e-4e0a-8ae1-a14c4f23b442">AddWorkItem</a> or <b>NewWorkItem</b>. When use <b>AddWorkItem</b>, it is your responsibility to create an instance of the Task object (which supports the <a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a> interface) and then add the task with the name you supply.



<b>NewWorkItem</b> does not prevent naming collisions, but requires only one disk write operation when <a href="_com_ipersistfile_save">IPersistFile::Save</a> is called. Although 
<b>NewWorkItem</b> is more efficient with respect to disk write operations, the application runs the risk of having another application create a work item with the same name before the call to <b>IPersistFile::Save</b> is made.


<table>
<tr>
<th>For a complete example of</th>
<th>See</th>
</tr>
<tr>
<td>Creating a new task</td>
<td>
<a href="https://msdn.microsoft.com/1cbdba6a-e017-4f00-87cb-970686a69e0a">Creating a Task Using NewWorkItem Example</a>
</td>
</tr>
</table>
 






## -see-also




<a href="_com_ipersistfile_save">IPersistFile::Save</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>



<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>



<a href="https://msdn.microsoft.com/5d776e19-c40e-4e0a-8ae1-a14c4f23b442">ITaskScheduler::AddWorkItem</a>
 

 

