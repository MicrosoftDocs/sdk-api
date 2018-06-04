---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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






#### - fWaitIfRunning [in]

Type: <b>BOOL</b>

<b>TRUE</b> if you want a currently running task to complete before removing it, <b>FALSE</b> otherwise.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



