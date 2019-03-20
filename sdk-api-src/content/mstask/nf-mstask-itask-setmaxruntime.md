---
UID: NF:mstask.ITask.SetMaxRunTime
title: ITask::SetMaxRunTime (mstask.h)
author: windows-sdk-content
description: This method sets the maximum time the task can run, in milliseconds, before terminating.
old-location: taskschd\itask_setmaxruntime.htm
tech.root: taskschd
ms.assetid: fb9012c6-be41-4ec6-bb1a-73bd7896738f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITask interface [Task Scheduler],SetMaxRunTime method, ITask.SetMaxRunTime, ITask::SetMaxRunTime, SetMaxRunTime, SetMaxRunTime method [Task Scheduler], SetMaxRunTime method [Task Scheduler],ITask interface, _msb_itask_setmaxruntime, mstask/ITask::SetMaxRunTime, taskschd.itask_setmaxruntime
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
 - ITask.SetMaxRunTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
---

# ITask::SetMaxRunTime


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

This method sets the maximum time the <a href="https://msdn.microsoft.com/en-us/library/Aa382533(v=VS.85).aspx">task</a> can run, in milliseconds, before terminating.


## -parameters




### -param dwMaxRunTimeMS [in]

A <b>DWORD</b> value that specifies the maximum run time (in milliseconds), for the task. This parameter may be set to INFINITE to specify an unlimited time.


## -returns



The 
<b>SetMaxRunTime</b> method returns one of the following values.

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



When the maximum run time is exceeded, the Task Scheduler attempts to terminate the application associated with the task. If a WM_CLOSE message cannot be sent (for example, the application has no windows) or the application has not exited within three minutes of the receiving WM_CLOSE, the Task Scheduler terminates the application using <b>TerminateProcess</b>.

After setting the maximum run time, be sure to call <b>IPersistFile::Save</b> to save the modified task object to disk.


#### Examples

For an example of how to set the maximum run time, see <a href="https://msdn.microsoft.com/ccfa3c01-870b-4b44-a493-9934ca1e51e4">C/C++ Code Example: Setting MaxRunTime</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/a9f27929-d304-4696-bb36-0c0a34c71388">IGetMaxRunTime</a>



<a href="https://msdn.microsoft.com/84a70dd0-43cb-42be-8360-35263bf1afb8">ITask</a>
 

 

