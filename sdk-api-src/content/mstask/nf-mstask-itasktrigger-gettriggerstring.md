---
UID: NF:mstask.ITaskTrigger.GetTriggerString
title: ITaskTrigger::GetTriggerString
author: windows-sdk-content
description: The GetTriggerString method retrieves the current task trigger in the form of a string. This string appears in the Task Scheduler user interface in a form similar to &#0034;At 2PM every day, starting 5/11/97.&#0034;.
old-location: taskschd\itasktrigger_gettriggerstring.htm
old-project: taskschd
ms.assetid: 5e21b61e-a43d-47b3-9380-b90d94e13cb8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTriggerString, GetTriggerString method [Task Scheduler], GetTriggerString method [Task Scheduler],ITaskTrigger interface, ITaskTrigger interface [Task Scheduler],GetTriggerString method, ITaskTrigger.GetTriggerString, ITaskTrigger::GetTriggerString, _msb_itasktrigger_gettriggerstring, mstask/ITaskTrigger::GetTriggerString, taskschd.itasktrigger_gettriggerstring
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskTrigger.GetTriggerString
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITaskTrigger::GetTriggerString


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>GetTriggerString</b> method retrieves the current task trigger in the form of a string. This string appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."


## -parameters




### -param ppwszTrigger [out]

A pointer to a pointer to a null-terminated string that describes the current task trigger. The method that invokes 
<b>GetTriggerString</b> is responsible for freeing this string using the <b>CoTaskMemFree</b> function.


## -returns



The 
<b>GetTriggerString</b> method returns one of the following values.

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




<a href="https://msdn.microsoft.com/990702f4-fb6f-47a7-b538-f6632f831a4e">ITaskTrigger</a>



<a href="https://msdn.microsoft.com/d6c9110d-c79e-475d-871b-83dca6577fc5">ITaskTrigger::GetTrigger</a>



<a href="https://msdn.microsoft.com/2f445835-a409-4a03-b853-4e0b07ded1ea">ITaskTrigger::SetTrigger</a>
 

 

