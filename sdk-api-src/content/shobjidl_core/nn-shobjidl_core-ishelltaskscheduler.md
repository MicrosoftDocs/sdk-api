---
UID: NN:shobjidl_core.IShellTaskScheduler
title: IShellTaskScheduler
author: windows-driver-content
description: IShellTaskScheduler may be altered or unavailable.
old-location: shell\IShellTaskScheduler.htm
old-project: shell
ms.assetid: 4898da7b-3d63-481f-a63a-d4f2554cfc8e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IShellTaskScheduler, IShellTaskScheduler interface [Windows Shell], IShellTaskScheduler interface [Windows Shell],described, _win32_IShellTaskScheduler, shell.IShellTaskScheduler, shobjidl_core/IShellTaskScheduler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IShellTaskScheduler
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IShellTaskScheduler interface


## -description


<p class="CCE_Message">[<b>IShellTaskScheduler</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Exposes methods that enable interaction with, and control of, a task scheduler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellTaskScheduler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IShellTaskScheduler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellTaskScheduler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227b5013-a550-46cc-bae2-af60776cba22">AddTask</a>
</td>
<td align="left" width="63%">
Adds a task to the scheduler's background queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41c0af40-35c2-4ce2-b9c3-246ee6268f49">CountTasks</a>
</td>
<td align="left" width="63%">
Counts tasks with the same owner ID in the scheduler's queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a160cfcf-f989-4a7c-9da0-97d658c151b9">RemoveTasks</a>
</td>
<td align="left" width="63%">
Removes tasks from the scheduler's background queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
</td>
<td align="left" width="63%">
Sets the release status and background thread timeout for the current task.

</td>
</tr>
</table> 


## -remarks



This interface does not need to be free-threaded unless the items in the queue interact with the scheduler as well as the main execution thread on which the task scheduler was created.

This interface's class identifier (CLSID) is CLSID_ShellTaskScheduler, and its IID is IID_IShellTaskScheduler.

<b>Windows Server 2003 and Windows XP:  </b><b>IShellTaskScheduler</b> was declared in Shlobj.h.



