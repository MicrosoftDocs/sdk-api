---
UID: NF:mstask.IScheduledWorkItem.GetRunTimes
title: IScheduledWorkItem::GetRunTimes
author: windows-sdk-content
description: Retrieves the work item run times for a specified time period.
old-location: taskschd\ischeduledworkitem_getruntimes.htm
tech.root: TaskSchd
ms.assetid: 4fd9f5dc-b237-46a6-96c0-0e4b3accd6e5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRunTimes, GetRunTimes method [Task Scheduler], GetRunTimes method [Task Scheduler],IScheduledWorkItem interface, IScheduledWorkItem interface [Task Scheduler],GetRunTimes method, IScheduledWorkItem.GetRunTimes, IScheduledWorkItem::GetRunTimes, _msb_ischeduledworkitem_getruntimes, mstask/IScheduledWorkItem::GetRunTimes, taskschd.ischeduledworkitem_getruntimes
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.GetRunTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
- apiref
: 
- COM
: 
- mstask.h
: 
- IScheduledWorkItem.GetRunTimes
: 
---

# IScheduledWorkItem::GetRunTimes


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Retrieves the <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a> run times for a specified time period.


## -parameters




### -param pstBegin [in]

A pointer to a <b>SYSTEMTIME</b> structure that contains the starting time of the time period to check. This value is inclusive.


### -param pstEnd [in]

A pointer to a <b>SYSTEMTIME</b> structure that contains the ending time of the time period to check. This value is exclusive. If <b>NULL</b> is passed for this value, the end time is infinite.


### -param pCount [in, out]

A pointer to a <b>WORD</b> value that specifies the number of run times to retrieve. 




On input, this parameter contains the number of run times being requested. This can be a number of between 1 and TASK_MAX_RUN_TIMES.

On output, this parameter contains the number of run times retrieved.


### -param rgstTaskTimes [out]

A pointer to an array of <b>SYSTEMTIME</b> structures. A <b>NULL</b> LPSYSTEMTIME object should be passed into this parameter. On return, this array contains <i>pCount</i> run times. You must free this array by a calling the <b>CoTaskMemFree</b> function.


## -returns



The 
<b>GetRunTimes</b> method returns one of the following values.

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
The requested number of run times was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded, but fewer than the requested number of run times were retrieved. The number of run times retrieved is contained in the value pointed to by <i>pCount</i>. If the number of run times retrieved is zero, there are also no event-based triggers that can cause the work item to be executed during the specified time period.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_TASK_NO_VALID_TRIGGERS</b></dt>
</dl>
</td>
<td width="60%">
The work item is enabled but has no valid triggers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_S_TASK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The work item is disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to compute the result.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e668833a-094d-4504-90a0-87912a6a53c2">IScheduledWorkItem</a>
 

 

