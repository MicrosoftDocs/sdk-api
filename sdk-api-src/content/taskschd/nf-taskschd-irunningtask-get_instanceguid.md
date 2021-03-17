---
UID: NF:taskschd.IRunningTask.get_InstanceGuid
title: IRunningTask::get_InstanceGuid (taskschd.h)
description: Gets the GUID identifier for this instance of the task.
helpviewer_keywords: ["IRunningTask interface [Task Scheduler]","InstanceGuid property","IRunningTask.InstanceGuid","IRunningTask.get_InstanceGuid","IRunningTask::InstanceGuid","IRunningTask::get_InstanceGuid","InstanceGuid property [Task Scheduler]","InstanceGuid property [Task Scheduler]","IRunningTask interface","get_InstanceGuid","taskschd.irunningtask_instanceguid","taskschd/IRunningTask::InstanceGuid","taskschd/IRunningTask::get_InstanceGuid"]
old-location: taskschd\irunningtask_instanceguid.htm
tech.root: taskschd
ms.assetid: 993682d1-c77c-48d8-bec6-aab810c8bcda
ms.date: 12/05/2018
ms.keywords: IRunningTask interface [Task Scheduler],InstanceGuid property, IRunningTask.InstanceGuid, IRunningTask.get_InstanceGuid, IRunningTask::InstanceGuid, IRunningTask::get_InstanceGuid, InstanceGuid property [Task Scheduler], InstanceGuid property [Task Scheduler],IRunningTask interface, get_InstanceGuid, taskschd.irunningtask_instanceguid, taskschd/IRunningTask::InstanceGuid, taskschd/IRunningTask::get_InstanceGuid
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunningTask::get_InstanceGuid
 - taskschd/IRunningTask::get_InstanceGuid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRunningTask.InstanceGuid
 - IRunningTask.get_InstanceGuid
---

# IRunningTask::get_InstanceGuid


## -description

Gets the GUID identifier for this instance of the task.

This property is read-only.

## -parameters

## -remarks

The <a href="/windows/desktop/api/taskschd/nf-taskschd-irunningtask-refresh">IRunningTask::Refresh</a> method is called before the property value is returned.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>