---
UID: NF:shobjidl_core.IShellTaskScheduler.RemoveTasks
title: IShellTaskScheduler::RemoveTasks
author: windows-sdk-content
description: Removes tasks from the scheduler's background queue.
old-location: shell\IShellTaskScheduler_RemoveTasks.htm
tech.root: shell
ms.assetid: a160cfcf-f989-4a7c-9da0-97d658c151b9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IShellTaskScheduler interface [Windows Shell],RemoveTasks method, IShellTaskScheduler.RemoveTasks, IShellTaskScheduler::RemoveTasks, RemoveTasks, RemoveTasks method [Windows Shell], RemoveTasks method [Windows Shell],IShellTaskScheduler interface, _win32_IShellTaskScheduler_RemoveTasks, shell.IShellTaskScheduler_RemoveTasks, shobjidl_core/IShellTaskScheduler::RemoveTasks
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
 - IShellTaskScheduler.RemoveTasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IShellTaskScheduler.RemoveTasks
: 
---

# IShellTaskScheduler::RemoveTasks


## -description


Removes tasks from the scheduler's background queue.


## -parameters




### -param rtoid [in]

Type: <b>REFTASKOWNERID</b>

A GUID identifying the owner of the tasks to remove.


### -param lParam [in]

Type: <b>DWORD_PTR</b>

A pointer to a user-defined <b>DWORD</b> value that allows the task to be identified within the tasks owned by <i>rtoid</i>. Set this value to 0 to remove all tasks for the owner specified by <i>rtoid</i>.
        


### -param bWaitIfRunning

TBD




#### - fWaitIfRunning [in]

Type: <b>BOOL</b>

<b>TRUE</b> if you want a currently running task to complete before removing it, <b>FALSE</b> otherwise.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



