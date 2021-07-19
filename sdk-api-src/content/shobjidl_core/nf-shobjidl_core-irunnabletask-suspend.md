---
UID: NF:shobjidl_core.IRunnableTask.Suspend
title: IRunnableTask::Suspend (shobjidl_core.h)
description: Requests that a task be suspended.
helpviewer_keywords: ["IRunnableTask interface [Windows Shell]","Suspend method","IRunnableTask.Suspend","IRunnableTask::Suspend","Suspend","Suspend method [Windows Shell]","Suspend method [Windows Shell]","IRunnableTask interface","_win32_IRunnableTask_Suspend","shell.IRunnableTask_Suspend","shobjidl_core/IRunnableTask::Suspend"]
old-location: shell\IRunnableTask_Suspend.htm
tech.root: shell
ms.assetid: f376d8e7-65d2-4824-a20f-e8604295df3f
ms.date: 12/05/2018
ms.keywords: IRunnableTask interface [Windows Shell],Suspend method, IRunnableTask.Suspend, IRunnableTask::Suspend, Suspend, Suspend method [Windows Shell], Suspend method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Suspend, shell.IRunnableTask_Suspend, shobjidl_core/IRunnableTask::Suspend
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
 - IRunnableTask::Suspend
 - shobjidl_core/IRunnableTask::Suspend
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
 - IRunnableTask.Suspend
---

# IRunnableTask::Suspend


## -description

Requests that a task be suspended.



## -returns

Type: <b>HRESULT</b>

Return S_OK if successful, or standard COM-defined error codes otherwise.

## -remarks

Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.

