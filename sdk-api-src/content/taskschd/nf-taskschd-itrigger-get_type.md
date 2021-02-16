---
UID: NF:taskschd.ITrigger.get_Type
title: ITrigger::get_Type (taskschd.h)
description: Gets the type of the trigger.
helpviewer_keywords: ["ITrigger interface [Task Scheduler]","Type property","ITrigger.Type","ITrigger.get_Type","ITrigger::Type","ITrigger::get_Type","TASK_TRIGGER_BOOT","TASK_TRIGGER_DAILY","TASK_TRIGGER_EVENT","TASK_TRIGGER_IDLE","TASK_TRIGGER_LOGON","TASK_TRIGGER_MONTHLY","TASK_TRIGGER_MONTHLYDOW","TASK_TRIGGER_REGISTRATION","TASK_TRIGGER_SESSION_STATE_CHANGE","TASK_TRIGGER_TIME","TASK_TRIGGER_WEEKLY","Type property [Task Scheduler]","Type property [Task Scheduler]","ITrigger interface","get_Type","taskschd.itrigger_type","taskschd/ITrigger::Type","taskschd/ITrigger::get_Type"]
old-location: taskschd\itrigger_type.htm
tech.root: taskschd
ms.assetid: 71e3915e-28d6-46fa-8f7a-8b4a6afa31c6
ms.date: 12/05/2018
ms.keywords: ITrigger interface [Task Scheduler],Type property, ITrigger.Type, ITrigger.get_Type, ITrigger::Type, ITrigger::get_Type, TASK_TRIGGER_BOOT, TASK_TRIGGER_DAILY, TASK_TRIGGER_EVENT, TASK_TRIGGER_IDLE, TASK_TRIGGER_LOGON, TASK_TRIGGER_MONTHLY, TASK_TRIGGER_MONTHLYDOW, TASK_TRIGGER_REGISTRATION, TASK_TRIGGER_SESSION_STATE_CHANGE, TASK_TRIGGER_TIME, TASK_TRIGGER_WEEKLY, Type property [Task Scheduler], Type property [Task Scheduler],ITrigger interface, get_Type, taskschd.itrigger_type, taskschd/ITrigger::Type, taskschd/ITrigger::get_Type
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
 - ITrigger::get_Type
 - taskschd/ITrigger::get_Type
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
 - ITrigger.Type
 - ITrigger.get_Type
---

# ITrigger::get_Type


## -description

Gets the type of the trigger. The trigger type is defined when the trigger is created and cannot be changed later. For information on creating a trigger, see <a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">ITriggerCollection::Create</a>



<a href="/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2">TASK_TRIGGER_TYPE2</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>