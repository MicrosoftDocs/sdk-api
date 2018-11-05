---
UID: NF:shobjidl_core.IShellTaskScheduler.CountTasks
title: IShellTaskScheduler::CountTasks
author: windows-sdk-content
description: Counts tasks with the same owner ID in the scheduler's queue.
old-location: shell\IShellTaskScheduler_CountTasks.htm
tech.root: shell
ms.assetid: 41c0af40-35c2-4ce2-b9c3-246ee6268f49
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CountTasks, CountTasks method [Windows Shell], CountTasks method [Windows Shell],IShellTaskScheduler interface, IShellTaskScheduler interface [Windows Shell],CountTasks method, IShellTaskScheduler.CountTasks, IShellTaskScheduler::CountTasks, _win32_IShellTaskScheduler_CountTasks, shell.IShellTaskScheduler_CountTasks, shobjidl_core/IShellTaskScheduler::CountTasks
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
 - IShellTaskScheduler.CountTasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellTaskScheduler::CountTasks


## -description


Counts tasks with the same owner ID in the scheduler's queue.


## -parameters




### -param rtoid [in]

Type: <b>REFTASKOWNERID</b>

A GUID identifying the owner of the tasks. Supplying a specific ID will count only those tasks tagged with that owner ID. To count all items in the queue, pass TOID_NULL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



