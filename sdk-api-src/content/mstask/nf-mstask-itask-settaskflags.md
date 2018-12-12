---
UID: NF:mstask.ITask.SetTaskFlags
title: ITask::SetTaskFlags
author: windows-sdk-content
description: This method sets the flags that modify the behavior of a scheduled task.
old-location: taskschd\itask_settaskflags.htm
tech.root: taskschd
ms.assetid: 32231145-241a-46ff-9c49-94f5bf7cc532
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITask interface [Task Scheduler],SetTaskFlags method, ITask.SetTaskFlags, ITask::SetTaskFlags, SetTaskFlags, SetTaskFlags method [Task Scheduler], SetTaskFlags method [Task Scheduler],ITask interface, _msb_itask_settaskflags, mstask/ITask::SetTaskFlags, taskschd.itask_settaskflags
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
 - ITask.SetTaskFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# ITask::SetTaskFlags


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the flags that modify the behavior of a scheduled <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">task</a>.


## -parameters




### -param dwFlags [in]

Currently, there are no flags defined for scheduled tasks.


## -returns



The 
<b>SetTaskFlags</b> method returns one of the following values.

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
 




## -remarks



Applications must call the <b>IPersistFile::Save</b> method after calling 
<b>SetTaskFlags</b> to update the task flags.

This method is designed to set the flags that only apply to scheduled tasks. In contrast, 
<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">IScheduledWorkItem::SetFlags</a> is used to set the flags that apply to all types of scheduled work items.




## -see-also




<a href="https://msdn.microsoft.com/fd919375-c903-45eb-a8f4-45baf5b42203">GetTaskFlags</a>



<a href="https://msdn.microsoft.com/640ba3c7-ed9d-4c4c-82fd-34fc777172c2">IScheduledWorkItem::SetFlags</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

