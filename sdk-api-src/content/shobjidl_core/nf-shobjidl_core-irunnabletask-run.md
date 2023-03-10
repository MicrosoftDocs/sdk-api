---
UID: NF:shobjidl_core.IRunnableTask.Run
title: IRunnableTask::Run (shobjidl_core.h)
description: Requests that a task begin.
helpviewer_keywords: ["IRunnableTask interface [Windows Shell]","Run method","IRunnableTask.Run","IRunnableTask::Run","Run","Run method [Windows Shell]","Run method [Windows Shell]","IRunnableTask interface","_win32_IRunnableTask_Run","shell.IRunnableTask_Run","shobjidl_core/IRunnableTask::Run"]
old-location: shell\IRunnableTask_Run.htm
tech.root: shell
ms.assetid: b929543c-d5b3-4d48-b13f-bbef568287a5
ms.date: 12/05/2018
ms.keywords: IRunnableTask interface [Windows Shell],Run method, IRunnableTask.Run, IRunnableTask::Run, Run, Run method [Windows Shell], Run method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Run, shell.IRunnableTask_Run, shobjidl_core/IRunnableTask::Run
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
 - IRunnableTask::Run
 - shobjidl_core/IRunnableTask::Run
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
 - IRunnableTask.Run
---

# IRunnableTask::Run


## -description

Requests that a task begin.



## -returns

Type: <b>HRESULT</b>

Returns one of the following two codes.

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
Execution is complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Execution is suspended.

</td>
</tr>
</table>

## -remarks

The return value of this method only tells you whether the execution of the task completed or is suspended. Any other errors that the implementer needs to communicate to the caller must be provided through other channels, such as a callback function.

