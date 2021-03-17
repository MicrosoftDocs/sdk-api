---
UID: NF:taskschd.ITaskService.NewTask
title: ITaskService::NewTask (taskschd.h)
description: Returns an empty task definition object to be filled in with settings and properties and then registered using the ITaskFolder::RegisterTaskDefinition method.
helpviewer_keywords: ["ITaskService interface [Task Scheduler]","NewTask method","ITaskService.NewTask","ITaskService::NewTask","NewTask","NewTask method [Task Scheduler]","NewTask method [Task Scheduler]","ITaskService interface","taskschd.itaskservice_newtask","taskschd/ITaskService::NewTask"]
old-location: taskschd\itaskservice_newtask.htm
tech.root: taskschd
ms.assetid: 821fc610-cf94-4548-950d-b4fd7b2f90dc
ms.date: 12/05/2018
ms.keywords: ITaskService interface [Task Scheduler],NewTask method, ITaskService.NewTask, ITaskService::NewTask, NewTask, NewTask method [Task Scheduler], NewTask method [Task Scheduler],ITaskService interface, taskschd.itaskservice_newtask, taskschd/ITaskService::NewTask
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskService::NewTask
 - taskschd/ITaskService::NewTask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskService.NewTask
---

# ITaskService::NewTask


## -description

Returns an empty task definition object to be filled in with settings and properties and then registered using the <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a> method.

## -parameters

### -param flags [in]

This parameter is reserved for future use and must be set to 0.

### -param ppDefinition [out]

The task definition that specifies all the information required to create a new task.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a> interface pointer. Referencing a non-NULL pointer can cause a memory leak because the pointer will be overwritten.

The returned <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a> pointer must be released after it is used.

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
<b>NULL</b> was passed in to the <i>ppDefinition</i> parameter. Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a> interface pointer.

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

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a>