---
UID: NF:taskschd.IRegisteredTask.get_Enabled
title: IRegisteredTask::get_Enabled (taskschd.h)
description: Gets or sets a Boolean value that indicates if the registered task is enabled. (Get)
helpviewer_keywords: ["Enabled property [Task Scheduler]","Enabled property [Task Scheduler]","IRegisteredTask interface","IRegisteredTask interface [Task Scheduler]","Enabled property","IRegisteredTask.Enabled","IRegisteredTask.get_Enabled","IRegisteredTask::Enabled","IRegisteredTask::get_Enabled","IRegisteredTask::put_Enabled","get_Enabled","taskschd.iregisteredtask_enabled","taskschd/IRegisteredTask::Enabled","taskschd/IRegisteredTask::get_Enabled","taskschd/IRegisteredTask::put_Enabled"]
old-location: taskschd\iregisteredtask_enabled.htm
tech.root: taskschd
ms.assetid: 33486621-3984-4a07-8182-c193847a9f76
ms.date: 12/05/2018
ms.keywords: Enabled property [Task Scheduler], Enabled property [Task Scheduler],IRegisteredTask interface, IRegisteredTask interface [Task Scheduler],Enabled property, IRegisteredTask.Enabled, IRegisteredTask.get_Enabled, IRegisteredTask::Enabled, IRegisteredTask::get_Enabled, IRegisteredTask::put_Enabled, get_Enabled, taskschd.iregisteredtask_enabled, taskschd/IRegisteredTask::Enabled, taskschd/IRegisteredTask::get_Enabled, taskschd/IRegisteredTask::put_Enabled
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
 - IRegisteredTask::get_Enabled
 - taskschd/IRegisteredTask::get_Enabled
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
 - IRegisteredTask.Enabled
 - IRegisteredTask.get_Enabled
 - IRegisteredTask.put_Enabled
---

# IRegisteredTask::get_Enabled


## -description

Gets or sets a Boolean value that indicates if the registered task is enabled.

This property is read/write.

## -parameters

## -remarks

This property is of type VARIANT_BOOL, which uses -1 to specify a true value and 0 to represent false. This property will not return an error if a value other than -1 or 0 is used.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask">IRegisteredTask</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
