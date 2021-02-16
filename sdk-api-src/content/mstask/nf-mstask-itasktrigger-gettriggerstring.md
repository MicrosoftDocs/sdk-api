---
UID: NF:mstask.ITaskTrigger.GetTriggerString
title: ITaskTrigger::GetTriggerString (mstask.h)
description: The GetTriggerString method retrieves the current task trigger in the form of a string. This string appears in the Task Scheduler user interface in a form similar to &quot;At 2PM every day, starting 5/11/97.&quot;.
helpviewer_keywords: ["GetTriggerString","GetTriggerString method [Task Scheduler]","GetTriggerString method [Task Scheduler]","ITaskTrigger interface","ITaskTrigger interface [Task Scheduler]","GetTriggerString method","ITaskTrigger.GetTriggerString","ITaskTrigger::GetTriggerString","_msb_itasktrigger_gettriggerstring","mstask/ITaskTrigger::GetTriggerString","taskschd.itasktrigger_gettriggerstring"]
old-location: taskschd\itasktrigger_gettriggerstring.htm
tech.root: taskschd
ms.assetid: 5e21b61e-a43d-47b3-9380-b90d94e13cb8
ms.date: 12/05/2018
ms.keywords: GetTriggerString, GetTriggerString method [Task Scheduler], GetTriggerString method [Task Scheduler],ITaskTrigger interface, ITaskTrigger interface [Task Scheduler],GetTriggerString method, ITaskTrigger.GetTriggerString, ITaskTrigger::GetTriggerString, _msb_itasktrigger_gettriggerstring, mstask/ITaskTrigger::GetTriggerString, taskschd.itasktrigger_gettriggerstring
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - ITaskTrigger::GetTriggerString
 - mstask/ITaskTrigger::GetTriggerString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskTrigger.GetTriggerString
---

# ITaskTrigger::GetTriggerString


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

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

<a href="/windows/desktop/api/mstask/nn-mstask-itasktrigger">ITaskTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-gettrigger">ITaskTrigger::GetTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itasktrigger-settrigger">ITaskTrigger::SetTrigger</a>