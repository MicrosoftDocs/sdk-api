---
UID: NF:mstask.ITaskScheduler.GetTargetComputer
title: ITaskScheduler::GetTargetComputer (mstask.h)
description: The GetTargetComputer method returns the name of the computer on which ITaskScheduler is currently targeted.
helpviewer_keywords: ["GetTargetComputer","GetTargetComputer method [Task Scheduler]","GetTargetComputer method [Task Scheduler]","ITaskScheduler interface","ITaskScheduler interface [Task Scheduler]","GetTargetComputer method","ITaskScheduler.GetTargetComputer","ITaskScheduler::GetTargetComputer","_msb_itaskscheduler_gettargetcomputer","mstask/ITaskScheduler::GetTargetComputer","taskschd.itaskscheduler_gettargetcomputer"]
old-location: taskschd\itaskscheduler_gettargetcomputer.htm
tech.root: taskschd
ms.assetid: c421a739-3290-4698-88e6-5c746baf903d
ms.date: 12/05/2018
ms.keywords: GetTargetComputer, GetTargetComputer method [Task Scheduler], GetTargetComputer method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],GetTargetComputer method, ITaskScheduler.GetTargetComputer, ITaskScheduler::GetTargetComputer, _msb_itaskscheduler_gettargetcomputer, mstask/ITaskScheduler::GetTargetComputer, taskschd.itaskscheduler_gettargetcomputer
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
 - ITaskScheduler::GetTargetComputer
 - mstask/ITaskScheduler::GetTargetComputer
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
 - ITaskScheduler.GetTargetComputer
---

# ITaskScheduler::GetTargetComputer


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>GetTargetComputer</b> method returns the name of the computer on which 
<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a> is currently targeted.

## -parameters

### -param ppwszComputer [out]

A pointer to a null-terminated string that contains the name of the target computer for the current task. This string is allocated by the application that invokes 
<b>GetTargetComputer</b>, and must also be freed using <b>CoTaskMemFree</b>.

## -returns

The 
<b>GetTargetComputer</b> method returns one of the following values.

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

<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a>