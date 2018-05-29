---
UID: NF:taskschd.ITaskService.NewTask
title: ITaskService::NewTask
author: windows-sdk-content
description: Returns an empty task definition object to be filled in with settings and properties and then registered using the ITaskFolder::RegisterTaskDefinition method.
old-location: taskschd\itaskservice_newtask.htm
old-project: TaskSchd
ms.assetid: 821fc610-cf94-4548-950d-b4fd7b2f90dc
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskService interface [Task Scheduler],NewTask method, ITaskService.NewTask, ITaskService::NewTask, NewTask, NewTask method [Task Scheduler], NewTask method [Task Scheduler],ITaskService interface, taskschd.itaskservice_newtask, taskschd/ITaskService::NewTask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskService.NewTask
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskService::NewTask


## -description


Returns an empty task definition object to be filled in with settings and properties and then registered using the <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a> method.


## -parameters




### -param flags [in]

This parameter is reserved for future use and must be set to 0.


### -param ppDefinition [out]

The task definition that specifies all the information required to create a new task.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a> interface pointer. Referencing a non-NULL pointer can cause a memory leak because the pointer will be overwritten.

The returned <a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a> pointer must be released after it is used.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
The method returned successfully without error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
<dt>0x80004003</dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> was passed in to the <i>ppDefinition</i> parameter. Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a> interface pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
A nonzero value was passed into the <i>flags</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2459aaae-4c3a-458a-ad2c-bfff3a0322d3">ITaskService</a>
 

 

