---
UID: NF:shobjidl_core.IRunnableTask.Kill
title: IRunnableTask::Kill
author: windows-sdk-content
description: Requests that a task be stopped.
old-location: shell\IRunnableTask_Kill.htm
old-project: shell
ms.assetid: 7465aded-43ff-4b63-8a90-b9f55240625b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IRunnableTask interface [Windows Shell],Kill method, IRunnableTask.Kill, IRunnableTask::Kill, Kill, Kill method [Windows Shell], Kill method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Kill, shell.IRunnableTask_Kill, shobjidl_core/IRunnableTask::Kill
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IRunnableTask.Kill
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IRunnableTask::Kill


## -description


Requests that a task be stopped.


## -parameters




### -param bWait






#### - fUnused

Type: <b>BOOL</b>

Not currently used.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.



