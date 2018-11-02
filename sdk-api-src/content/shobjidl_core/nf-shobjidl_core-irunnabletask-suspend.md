---
UID: NF:shobjidl_core.IRunnableTask.Suspend
title: IRunnableTask::Suspend
author: windows-sdk-content
description: Requests that a task be suspended.
old-location: shell\IRunnableTask_Suspend.htm
tech.root: shell
ms.assetid: f376d8e7-65d2-4824-a20f-e8604295df3f
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IRunnableTask interface [Windows Shell],Suspend method, IRunnableTask.Suspend, IRunnableTask::Suspend, Suspend, Suspend method [Windows Shell], Suspend method [Windows Shell],IRunnableTask interface, _win32_IRunnableTask_Suspend, shell.IRunnableTask_Suspend, shobjidl_core/IRunnableTask::Suspend
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRunnableTask.Suspend
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunnableTask::Suspend


## -description


Requests that a task be suspended.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or standard COM-defined error codes otherwise.




## -remarks



Implementation of this method is optional. If you do not wish to support this functionality, create a token implementation that simply returns E_NOTIMPL.



