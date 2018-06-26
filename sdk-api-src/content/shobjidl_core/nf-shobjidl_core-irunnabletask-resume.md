---
UID: NF:shobjidl_core.IRunnableTask.Resume
title: IRunnableTask::Resume
author: windows-sdk-content
description: Requests that a task resume.
old-location: shell\IRunnableTask_Resume.htm
old-project: shell
ms.assetid: 51ff7ae2-b2db-4eee-b03b-da46ff0ec901
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: IRunnableTask interface [Windows Shell],Resume method, IRunnableTask.Resume, IRunnableTask::Resume, Resume, Resume method [Windows Shell], Resume method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Resume, shell.IRunnableTask_Resume, shobjidl_core/IRunnableTask::Resume
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IRunnableTask.Resume
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IRunnableTask::Resume


## -description


Requests that a task resume.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or standard COM-defined error codes otherwise.




## -remarks



Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.



