---
UID: NF:shobjidl_core.IRunnableTask.Resume
title: IRunnableTask::Resume (shobjidl_core.h)
description: Requests that a task resume.
helpviewer_keywords: ["IRunnableTask interface [Windows Shell]","Resume method","IRunnableTask.Resume","IRunnableTask::Resume","Resume","Resume method [Windows Shell]","Resume method [Windows Shell]","IRunnableTask interface","_win32_IRunnableTask_Resume","shell.IRunnableTask_Resume","shobjidl_core/IRunnableTask::Resume"]
old-location: shell\IRunnableTask_Resume.htm
tech.root: shell
ms.assetid: 51ff7ae2-b2db-4eee-b03b-da46ff0ec901
ms.date: 12/05/2018
ms.keywords: IRunnableTask interface [Windows Shell],Resume method, IRunnableTask.Resume, IRunnableTask::Resume, Resume, Resume method [Windows Shell], Resume method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Resume, shell.IRunnableTask_Resume, shobjidl_core/IRunnableTask::Resume
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
 - IRunnableTask::Resume
 - shobjidl_core/IRunnableTask::Resume
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
 - IRunnableTask.Resume
---

# IRunnableTask::Resume


## -description

Requests that a task resume.



## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or standard COM-defined error codes otherwise.

## -remarks

Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.

