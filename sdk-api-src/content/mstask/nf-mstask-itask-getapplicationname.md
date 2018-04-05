---
UID: NF:mstask.ITask.GetApplicationName
title: ITask::GetApplicationName method
author: windows-driver-content
description: This method retrieves the name of the application that the task is associated with.
old-location: taskschd\itask_getapplicationname.htm
old-project: TaskSchd
ms.assetid: 79a8c324-1191-412b-be2b-eb5935337925
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetApplicationName method [Task Scheduler], GetApplicationName method [Task Scheduler], ITask interface, GetApplicationName,ITask.GetApplicationName, ITask, ITask interface [Task Scheduler], GetApplicationName method, ITask::GetApplicationName, _msb_itask_getapplicationname, mstask/ITask::GetApplicationName, taskschd.itask_getapplicationname
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
-	ITask.GetApplicationName
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITask::GetApplicationName method


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method retrieves the name of the application that the <a href="t.htm">task</a> is associated with.


## -parameters




### -param ppwszApplicationName [out]

A pointer to a null-terminated string that contains the name of the application the current task is associated with. After processing this name, call <b>CoTaskMemFree</b> to free resources.


## -returns



The 
<b>GetApplicationName</b> method returns one of the following values.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>



<a href="https://msdn.microsoft.com/0bec25a9-e653-48b5-be41-8f513169fc8c">ITask::SetApplicationName</a>



<a href="https://msdn.microsoft.com/094dcd8f-35aa-4300-b58d-c846bca1c88c">SetParameters</a>
 

 

