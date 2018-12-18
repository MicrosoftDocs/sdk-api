---
UID: NF:mstask.ITaskScheduler.Activate
title: ITaskScheduler::Activate
author: windows-sdk-content
description: The Activate method returns an active interface for a specified work item.
old-location: taskschd\itaskscheduler_activate.htm
tech.root: taskschd
ms.assetid: 27391e34-8632-4ab5-9d6e-d2fde7942f80
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Activate, Activate method [Task Scheduler], Activate method [Task Scheduler],ITaskScheduler interface, ITaskScheduler interface [Task Scheduler],Activate method, ITaskScheduler.Activate, ITaskScheduler::Activate, _msb_itaskscheduler_activate, mstask/ITaskScheduler::Activate, taskschd.itaskscheduler_activate
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
 - ITaskScheduler.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# ITaskScheduler::Activate


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>Activate</b> method returns an active interface for a specified <a href="https://msdn.microsoft.com/en-us/library/Aa384011(v=VS.85).aspx">work item</a>.


## -parameters




### -param pwszName [in]

A null-terminated string that specifies the name of the work item to activate.


### -param riid [in]

An identifier that identifies the interface being requested. The only interface supported at this time, 
<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>, has the identifier IID_ITask.


### -param ppUnk [out]

A pointer to an interface pointer that receives the address of the requested interface.


## -returns



When 
this method succeeds, S_OK is returned.

If the method fails, one of the following error codes may be returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COR_E_FILENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The task does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszName</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_UNKNOWN_OBJECT_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The task object version is either unsupported or invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>



<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>
 

 

