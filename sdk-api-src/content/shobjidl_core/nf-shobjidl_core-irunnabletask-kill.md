---
UID: NF:shobjidl_core.IRunnableTask.Kill
title: IRunnableTask::Kill (shobjidl_core.h)
description: Requests that a task be stopped.
helpviewer_keywords: ["IRunnableTask interface [Windows Shell]","Kill method","IRunnableTask.Kill","IRunnableTask::Kill","Kill","Kill method [Windows Shell]","Kill method [Windows Shell]","IRunnableTask interface","_win32_IRunnableTask_Kill","shell.IRunnableTask_Kill","shobjidl_core/IRunnableTask::Kill"]
old-location: shell\IRunnableTask_Kill.htm
tech.root: shell
ms.assetid: 7465aded-43ff-4b63-8a90-b9f55240625b
ms.date: 12/05/2018
ms.keywords: IRunnableTask interface [Windows Shell],Kill method, IRunnableTask.Kill, IRunnableTask::Kill, Kill, Kill method [Windows Shell], Kill method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Kill, shell.IRunnableTask_Kill, shobjidl_core/IRunnableTask::Kill
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
 - IRunnableTask::Kill
 - shobjidl_core/IRunnableTask::Kill
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
 - IRunnableTask.Kill
---

# IRunnableTask::Kill


## -description

Requests that a task be stopped.

## -parameters

### -param bWait

Type: <b>BOOL</b>

Not currently used.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.

