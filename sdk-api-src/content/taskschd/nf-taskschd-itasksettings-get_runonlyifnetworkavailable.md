---
UID: NF:taskschd.ITaskSettings.get_RunOnlyIfNetworkAvailable
title: ITaskSettings::get_RunOnlyIfNetworkAvailable (taskschd.h)
description: Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available. (Get)
helpviewer_keywords: ["ITaskSettings interface [Task Scheduler]","RunOnlyIfNetworkAvailable property","ITaskSettings.RunOnlyIfNetworkAvailable","ITaskSettings.get_RunOnlyIfNetworkAvailable","ITaskSettings::RunOnlyIfNetworkAvailable","ITaskSettings::get_RunOnlyIfNetworkAvailable","ITaskSettings::put_RunOnlyIfNetworkAvailable","RunOnlyIfNetworkAvailable property [Task Scheduler]","RunOnlyIfNetworkAvailable property [Task Scheduler]","ITaskSettings interface","get_RunOnlyIfNetworkAvailable","taskschd.itasksettings_runonlyifnetworkavailable","taskschd/ITaskSettings::RunOnlyIfNetworkAvailable","taskschd/ITaskSettings::get_RunOnlyIfNetworkAvailable","taskschd/ITaskSettings::put_RunOnlyIfNetworkAvailable"]
old-location: taskschd\itasksettings_runonlyifnetworkavailable.htm
tech.root: taskschd
ms.assetid: d0926d75-e7d9-469c-aaa0-ddee8fe22dcd
ms.date: 12/05/2018
ms.keywords: ITaskSettings interface [Task Scheduler],RunOnlyIfNetworkAvailable property, ITaskSettings.RunOnlyIfNetworkAvailable, ITaskSettings.get_RunOnlyIfNetworkAvailable, ITaskSettings::RunOnlyIfNetworkAvailable, ITaskSettings::get_RunOnlyIfNetworkAvailable, ITaskSettings::put_RunOnlyIfNetworkAvailable, RunOnlyIfNetworkAvailable property [Task Scheduler], RunOnlyIfNetworkAvailable property [Task Scheduler],ITaskSettings interface, get_RunOnlyIfNetworkAvailable, taskschd.itasksettings_runonlyifnetworkavailable, taskschd/ITaskSettings::RunOnlyIfNetworkAvailable, taskschd/ITaskSettings::get_RunOnlyIfNetworkAvailable, taskschd/ITaskSettings::put_RunOnlyIfNetworkAvailable
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
 - ITaskSettings::get_RunOnlyIfNetworkAvailable
 - taskschd/ITaskSettings::get_RunOnlyIfNetworkAvailable
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
 - ITaskSettings.RunOnlyIfNetworkAvailable
 - ITaskSettings.get_RunOnlyIfNetworkAvailable
 - ITaskSettings.put_RunOnlyIfNetworkAvailable
---

# ITaskSettings::get_RunOnlyIfNetworkAvailable


## -description

Gets or sets a Boolean value that indicates that the Task Scheduler will run the task only when a network is available.

This property is read/write.

## -parameters

## -remarks

When reading or writing  XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-runonlyifnetworkavailable-settingstype-element">RunOnlyIfNetworkAvailable</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
