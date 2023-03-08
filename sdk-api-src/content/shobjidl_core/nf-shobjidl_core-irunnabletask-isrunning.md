---
UID: NF:shobjidl_core.IRunnableTask.IsRunning
title: IRunnableTask::IsRunning (shobjidl_core.h)
description: Requests information on the state of a task, such as thumbnail extraction.
helpviewer_keywords: ["IRunnableTask interface [Windows Shell]","IsRunning method","IRunnableTask.IsRunning","IRunnableTask::IsRunning","IsRunning","IsRunning method [Windows Shell]","IsRunning method [Windows Shell]","IRunnableTask interface","_win32_IRunnableTask_IsRunning","shell.IRunnableTask_IsRunning","shobjidl_core/IRunnableTask::IsRunning"]
old-location: shell\IRunnableTask_IsRunning.htm
tech.root: shell
ms.assetid: 14117a47-d462-4be1-b440-8d422c938815
ms.date: 12/05/2018
ms.keywords: IRunnableTask interface [Windows Shell],IsRunning method, IRunnableTask.IsRunning, IRunnableTask::IsRunning, IsRunning, IsRunning method [Windows Shell], IsRunning method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_IsRunning, shell.IRunnableTask_IsRunning, shobjidl_core/IRunnableTask::IsRunning
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunnableTask::IsRunning
 - shobjidl_core/IRunnableTask::IsRunning
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRunnableTask.IsRunning
---

# IRunnableTask::IsRunning


## -description

Requests information on the state of a task, such as thumbnail extraction.



## -returns

Type: <b>LONG</b>

Returns one of the following values to indicate the current execution state.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
Extraction has not yet started.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The task is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_SUSPENDED</b></dt>
</dl>
</td>
<td width="60%">
The task is suspended.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_PENDING</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-irunnabletask-kill">IRunnableTask::Kill</a> has been called on the thread, but the thread has not yet completely shut down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IRTIR_TASK_FINISHED</b></dt>
</dl>
</td>
<td width="60%">
The task is finished.

</td>
</tr>
</table>

## -remarks

This method must be implemented.
