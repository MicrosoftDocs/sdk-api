---
UID: NF:shobjidl_core.IShellTaskScheduler.Status
title: IShellTaskScheduler::Status (shobjidl_core.h)
description: Sets the release status and background thread timeout for the current task.
helpviewer_keywords: ["IShellTaskScheduler interface [Windows Shell]","Status method","IShellTaskScheduler.Status","IShellTaskScheduler::Status","ITSSFLAG_KILL_ON_DESTROY","Status","Status method [Windows Shell]","Status method [Windows Shell]","IShellTaskScheduler interface","_win32_IShellTaskScheduler_Status","shell.IShellTaskScheduler_Status","shobjidl_core/IShellTaskScheduler::Status"]
old-location: shell\IShellTaskScheduler_Status.htm
tech.root: shell
ms.assetid: 378a2ae1-520a-48a7-a2e5-fa1ad25e2380
ms.date: 12/05/2018
ms.keywords: IShellTaskScheduler interface [Windows Shell],Status method, IShellTaskScheduler.Status, IShellTaskScheduler::Status, ITSSFLAG_KILL_ON_DESTROY, Status, Status method [Windows Shell], Status method [Windows Shell],IShellTaskScheduler interface, _win32_IShellTaskScheduler_Status, shell.IShellTaskScheduler_Status, shobjidl_core/IShellTaskScheduler::Status
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
 - IShellTaskScheduler::Status
 - shobjidl_core/IShellTaskScheduler::Status
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
 - IShellTaskScheduler.Status
---

# IShellTaskScheduler::Status


## -description

Sets the release status and background thread timeout for the current task.

## -parameters

### -param dwReleaseStatus [in]

Type: <b>DWORD</b>

The following flag or 0.



#### ITSSFLAG_KILL_ON_DESTROY

Immediately cease execution of the current task when the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelltaskscheduler">IShellTaskScheduler</a> instance is released.

### -param dwThreadTimeout [in]

Type: <b>DWORD</b>

Not used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.