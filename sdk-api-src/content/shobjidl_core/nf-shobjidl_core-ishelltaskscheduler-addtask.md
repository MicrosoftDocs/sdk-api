---
UID: NF:shobjidl_core.IShellTaskScheduler.AddTask
title: IShellTaskScheduler::AddTask
author: windows-sdk-content
description: Adds a task to the scheduler's background queue.
old-location: shell\IShellTaskScheduler_AddTask.htm
tech.root: shell
ms.assetid: 227b5013-a550-46cc-bae2-af60776cba22
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AddTask, AddTask method [Windows Shell], AddTask method [Windows Shell],IShellTaskScheduler interface, IShellTaskScheduler interface [Windows Shell],AddTask method, IShellTaskScheduler.AddTask, IShellTaskScheduler::AddTask, ITSAT_DEFAULT_PRIORITY, ITSAT_MAX_PRIORITY, ITSAT_MIN_PRIORITY, _win32_IShellTaskScheduler_AddTask, shell.IShellTaskScheduler_AddTask, shobjidl_core/IShellTaskScheduler::AddTask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IShellTaskScheduler.AddTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellTaskScheduler::AddTask


## -description


Adds a task to the scheduler's background queue.


## -parameters




### -param prt

TBD


### -param rtoid [in]

Type: <b>REFTASKOWNERID</b>

A GUID identifying the owner of the task. This information can be used to group tasks for later <a href="https://msdn.microsoft.com/41c0af40-35c2-4ce2-b9c3-246ee6268f49">counting</a> or <a href="https://msdn.microsoft.com/a160cfcf-f989-4a7c-9da0-97d658c151b9">removal</a> by owner.


### -param lParam [in]

Type: <b>DWORD_PTR</b>

A pointer to a user-defined <b>DWORD</b> value allowing the task to be identified within the tasks owned by <i>rtoid</i>. This is used to identify single tasks or to subgroup them, for instance associating the task with a particular item such as an item in a ListView. This parameter can be zero.


### -param dwPriority [in]

Type: <b>DWORD</b>

One of the following values assigning the task's priority. Response to this priority depends on the cooperation of the other tasks being executed. New tasks are inserted in the queue in priority order. If a task of a low priority is currently under execution when a higher priority task is added, the scheduler attempts to suspend the task under execution. That lower priority task is resumed when the higher priority task(s) are completed.



#### ITSAT_DEFAULT_PRIORITY

Accept the default priority assigned to the task by the scheduler.



#### ITSAT_MAX_PRIORITY

High priority.



#### ITSAT_MIN_PRIORITY

Low priority.


#### - pTask [in]

Type: <b><a href="https://msdn.microsoft.com/158a6688-949b-4075-a790-fd6efb88792c">IRunnableTask</a>*</b>

A pointer to an instance of an <a href="https://msdn.microsoft.com/158a6688-949b-4075-a790-fd6efb88792c">IRunnableTask</a> interface representing the task to add to the queue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



