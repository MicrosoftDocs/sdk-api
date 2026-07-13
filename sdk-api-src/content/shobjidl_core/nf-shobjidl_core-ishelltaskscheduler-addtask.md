---
UID: NF:shobjidl_core.IShellTaskScheduler.AddTask
title: IShellTaskScheduler::AddTask (shobjidl_core.h)
description: Adds a task to the scheduler's background queue.
helpviewer_keywords: ["AddTask","AddTask method [Windows Shell]","AddTask method [Windows Shell]","IShellTaskScheduler interface","IShellTaskScheduler interface [Windows Shell]","AddTask method","IShellTaskScheduler.AddTask","IShellTaskScheduler::AddTask","ITSAT_DEFAULT_PRIORITY","ITSAT_MAX_PRIORITY","ITSAT_MIN_PRIORITY","_win32_IShellTaskScheduler_AddTask","shell.IShellTaskScheduler_AddTask","shobjidl_core/IShellTaskScheduler::AddTask"]
old-location: shell\IShellTaskScheduler_AddTask.htm
tech.root: shell
ms.assetid: 227b5013-a550-46cc-bae2-af60776cba22
ms.date: 12/05/2018
ms.keywords: AddTask, AddTask method [Windows Shell], AddTask method [Windows Shell],IShellTaskScheduler interface, IShellTaskScheduler interface [Windows Shell],AddTask method, IShellTaskScheduler.AddTask, IShellTaskScheduler::AddTask, ITSAT_DEFAULT_PRIORITY, ITSAT_MAX_PRIORITY, ITSAT_MIN_PRIORITY, _win32_IShellTaskScheduler_AddTask, shell.IShellTaskScheduler_AddTask, shobjidl_core/IShellTaskScheduler::AddTask
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellTaskScheduler::AddTask
 - shobjidl_core/IShellTaskScheduler::AddTask
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
 - IShellTaskScheduler.AddTask
---

# IShellTaskScheduler::AddTask


## -description

Adds a task to the scheduler's background queue.

## -parameters

### -param prt [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask">IRunnableTask</a>*</b>

A pointer to an instance of an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask">IRunnableTask</a> interface representing the task to add to the queue.

### -param rtoid [in]

Type: <b>REFTASKOWNERID</b>

A GUID identifying the owner of the task. This information can be used to group tasks for later <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelltaskscheduler-counttasks">counting</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelltaskscheduler-removetasks">removal</a> by owner.

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

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.