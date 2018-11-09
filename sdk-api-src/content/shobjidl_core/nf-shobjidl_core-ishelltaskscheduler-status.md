---
UID: NF:shobjidl_core.IShellTaskScheduler.Status
title: IShellTaskScheduler::Status
author: windows-sdk-content
description: Sets the release status and background thread timeout for the current task.
old-location: shell\IShellTaskScheduler_Status.htm
tech.root: shell
ms.assetid: 378a2ae1-520a-48a7-a2e5-fa1ad25e2380
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IShellTaskScheduler interface [Windows Shell],Status method, IShellTaskScheduler.Status, IShellTaskScheduler::Status, ITSSFLAG_KILL_ON_DESTROY, Status, Status method [Windows Shell], Status method [Windows Shell],IShellTaskScheduler interface, _win32_IShellTaskScheduler_Status, shell.IShellTaskScheduler_Status, shobjidl_core/IShellTaskScheduler::Status
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
 - IShellTaskScheduler.Status
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellTaskScheduler::Status


## -description


Sets the release status and background thread timeout for the current task.


## -parameters




### -param dwReleaseStatus [in]

Type: <b>DWORD</b>

The following flag or 0.



#### ITSSFLAG_KILL_ON_DESTROY

Immediately cease execution of the current task when the <a href="https://msdn.microsoft.com/4898da7b-3d63-481f-a63a-d4f2554cfc8e">IShellTaskScheduler</a> instance is released.


### -param dwThreadTimeout [in]

Type: <b>DWORD</b>

Not used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



