---
UID: NF:taskschd.ITaskSettings.put_DeleteExpiredTaskAfter
title: ITaskSettings::put_DeleteExpiredTaskAfter (taskschd.h)
description: Gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires. (Put)
helpviewer_keywords: ["DeleteExpiredTaskAfter property [Task Scheduler]","DeleteExpiredTaskAfter property [Task Scheduler]","ITaskSettings interface","ITaskSettings interface [Task Scheduler]","DeleteExpiredTaskAfter property","ITaskSettings.DeleteExpiredTaskAfter","ITaskSettings.put_DeleteExpiredTaskAfter","ITaskSettings::DeleteExpiredTaskAfter","ITaskSettings::get_DeleteExpiredTaskAfter","ITaskSettings::put_DeleteExpiredTaskAfter","put_DeleteExpiredTaskAfter","taskschd.itasksettings_deleteexpiredtaskafter","taskschd/ITaskSettings::DeleteExpiredTaskAfter","taskschd/ITaskSettings::get_DeleteExpiredTaskAfter","taskschd/ITaskSettings::put_DeleteExpiredTaskAfter"]
old-location: taskschd\itasksettings_deleteexpiredtaskafter.htm
tech.root: taskschd
ms.assetid: c6a2a12d-a41a-4fd8-a328-bce0fe19deba
ms.date: 12/05/2018
ms.keywords: DeleteExpiredTaskAfter property [Task Scheduler], DeleteExpiredTaskAfter property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],DeleteExpiredTaskAfter property, ITaskSettings.DeleteExpiredTaskAfter, ITaskSettings.put_DeleteExpiredTaskAfter, ITaskSettings::DeleteExpiredTaskAfter, ITaskSettings::get_DeleteExpiredTaskAfter, ITaskSettings::put_DeleteExpiredTaskAfter, put_DeleteExpiredTaskAfter, taskschd.itasksettings_deleteexpiredtaskafter, taskschd/ITaskSettings::DeleteExpiredTaskAfter, taskschd/ITaskSettings::get_DeleteExpiredTaskAfter, taskschd/ITaskSettings::put_DeleteExpiredTaskAfter
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
 - ITaskSettings::put_DeleteExpiredTaskAfter
 - taskschd/ITaskSettings::put_DeleteExpiredTaskAfter
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
 - ITaskSettings.DeleteExpiredTaskAfter
 - ITaskSettings.get_DeleteExpiredTaskAfter
 - ITaskSettings.put_DeleteExpiredTaskAfter
---

# ITaskSettings::put_DeleteExpiredTaskAfter


## -description

Gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires. If no value  is specified for this property, then the Task Scheduler service will not delete the task.

This property is read/write.

## -parameters

## -remarks

A task expires after the end boundary has been exceeded for all triggers associated with the task. The end boundary for a trigger is specified by the <a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary">EndBoundary</a> property inherited by all trigger interfaces.

When reading or writing XML for a task, this setting is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-deleteexpiredtaskafter-settingstype-element">DeleteExpiredTaskAfter (settingsType)</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasksettings">ITaskSettings</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
