---
UID: NF:shobjidl_core.IRunnableTask.Run
title: IRunnableTask::Run
author: windows-sdk-content
description: Requests that a task begin.
old-location: shell\IRunnableTask_Run.htm
tech.root: Shell
ms.assetid: b929543c-d5b3-4d48-b13f-bbef568287a5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IRunnableTask interface [Windows Shell],Run method, IRunnableTask.Run, IRunnableTask::Run, Run, Run method [Windows Shell], Run method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Run, shell.IRunnableTask_Run, shobjidl_core/IRunnableTask::Run
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRunnableTask.Run
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunnableTask::Run


## -description


Requests that a task begin.


## -parameters






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



