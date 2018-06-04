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

# IShellTaskScheduler::AddTask


## -description


Adds a task to the scheduler's background queue.


## -parameters




### -param prt




### -param rtoid [in]

Type: <b>REFTASKOWNERID</b>

A GUID identifying the owner of the task. This information can be used to group tasks for later <a href="https://msdn.microsoft.com/41c0af40-35c2-4ce2-b9c3-246ee6268f49">counting</a> or <a href="https://msdn.microsoft.com/a160cfcf-f989-4a7c-9da0-97d658c151b9">removal</a> by owner.


### -param lParam [in]

Type: <b>DWORD_PTR</b>

A pointer to a user-defined <b>DWORD</b> value allowing the task to be identified within the tasks owned by <i>rtoid</i>. This is used to identify single tasks or to subgroup them, for instance associating the task with a particular item such as an item in a ListView. This parameter can be zero.


### -param dwPriority [in]

Type: <b>DWORD</b>

One of the following values assigning the task's priority. Response to this priority depends on the cooperation of the other tasks being executed. New tasks are inserted in the queue in priority order. If a task of a low priority is currently under execution when a higher priority task is added, the scheduler attempts to suspend the task under execution. That lower priority task is resumed when the higher priority task(s) are completed.



#### ITSAT_DEFAULT_PRIORITY

Accept the default priority assigned to the task by the scheduler.



#### ITSAT_MAX_PRIORITY

High priority.



#### ITSAT_MIN_PRIORITY

Low priority.


#### - pTask [in]

Type: <b><a href="https://msdn.microsoft.com/158a6688-949b-4075-a790-fd6efb88792c">IRunnableTask</a>*</b>

A pointer to an instance of an <a href="https://msdn.microsoft.com/158a6688-949b-4075-a790-fd6efb88792c">IRunnableTask</a> interface representing the task to add to the queue.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



