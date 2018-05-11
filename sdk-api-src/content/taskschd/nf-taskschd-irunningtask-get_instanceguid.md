---
UID: NF:taskschd.IRunningTask.get_InstanceGuid
title: IRunningTask::get_InstanceGuid
author: windows-driver-content
description: Gets the GUID identifier for this instance of the task.
old-location: taskschd\irunningtask_instanceguid.htm
old-project: TaskSchd
ms.assetid: 993682d1-c77c-48d8-bec6-aab810c8bcda
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IRunningTask interface [Task Scheduler],InstanceGuid property, IRunningTask.InstanceGuid, IRunningTask.get_InstanceGuid, IRunningTask::InstanceGuid, IRunningTask::get_InstanceGuid, InstanceGuid property [Task Scheduler], InstanceGuid property [Task Scheduler],IRunningTask interface, get_InstanceGuid, taskschd.irunningtask_instanceguid, taskschd/IRunningTask::InstanceGuid, taskschd/IRunningTask::get_InstanceGuid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IRunningTask.InstanceGuid
-	IRunningTask.get_InstanceGuid
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRunningTask::get_InstanceGuid


## -description


Gets the GUID identifier for this instance of the task.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/f46d82ff-2f1b-477b-b043-665659ad8982">IRunningTask::Refresh</a> method is called before the property value is returned.




## -see-also




<a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

