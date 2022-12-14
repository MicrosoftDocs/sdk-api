---
UID: NF:taskschd.ITaskSettings.put_Compatibility
title: ITaskSettings::put_Compatibility (taskschd.h)
description: Gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with. (Put)
helpviewer_keywords: ["Compatibility property [Task Scheduler]","Compatibility property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","Compatibility property","ITaskSettings.Compatibility","ITaskSettings.put_Compatibility","ITaskSettings::Compatibility","ITaskSettings::get_Compatibility","ITaskSettings::put_Compatibility","TASK_COMPATIBILITY_AT","TASK_COMPATIBILITY_V1","TASK_COMPATIBILITY_V2","put_Compatibility","taskschd.itasksettings_compatibility","taskschd/ITaskSettings::Compatibility","taskschd/ITaskSettings::get_Compatibility","taskschd/ITaskSettings::put_Compatibility"]
old-location: taskschd\itasksettings_compatibility.htm
tech.root: taskschd
ms.assetid: 04f77d3c-44fa-4091-b99e-af062f067ef9
ms.date: 12/05/2018
ms.keywords: Compatibility property [Task Scheduler], Compatibility property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],Compatibility property, ITaskSettings.Compatibility, ITaskSettings.put_Compatibility, ITaskSettings::Compatibility, ITaskSettings::get_Compatibility, ITaskSettings::put_Compatibility, TASK_COMPATIBILITY_AT, TASK_COMPATIBILITY_V1, TASK_COMPATIBILITY_V2, put_Compatibility, taskschd.itasksettings_compatibility, taskschd/ITaskSettings::Compatibility, taskschd/ITaskSettings::get_Compatibility, taskschd/ITaskSettings::put_Compatibility
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
 - ITaskSettings::put_Compatibility
 - taskschd/ITaskSettings::put_Compatibility
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
 - ITaskSettings.Compatibility
 - ITaskSettings.get_Compatibility
 - ITaskSettings.put_Compatibility
---

# ITaskSettings::put_Compatibility


## -description

Gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.

This property is read/write.

## -parameters

## -remarks

 Task compatibility, which is set through the <b>Compatibility</b> property, should only be set to TASK_COMPATIBILITY_V1 if a task needs to be accessed or modified from a  Windows XP, Windows Server 2003, or Windows 2000 computer. Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.

Tasks compatible with the AT command can only have one time trigger.

Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.

For more information about task compatibility, see <a href="/windows/desktop/TaskSchd/what-s-new-in-task-scheduler">What's New in Task Scheduler</a> and <a href="/windows/desktop/TaskSchd/tasks">Tasks</a>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_compatibility">TASK_COMPATIBILITY</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
