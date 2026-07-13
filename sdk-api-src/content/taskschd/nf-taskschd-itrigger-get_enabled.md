---
UID: NF:taskschd.ITrigger.get_Enabled
title: ITrigger::get_Enabled (taskschd.h)
description: Gets or sets a Boolean value that indicates whether the trigger is enabled. (Get)
helpviewer_keywords: ["Enabled property [Task Scheduler]","Enabled property [Task Scheduler]","ITrigger interface","ITrigger interface [Task Scheduler]","Enabled property","ITrigger.Enabled","ITrigger.get_Enabled","ITrigger::Enabled","ITrigger::get_Enabled","ITrigger::put_Enabled","get_Enabled","taskschd.itrigger_enabled","taskschd/ITrigger::Enabled","taskschd/ITrigger::get_Enabled","taskschd/ITrigger::put_Enabled"]
old-location: taskschd\itrigger_enabled.htm
tech.root: taskschd
ms.assetid: 20300470-e434-4296-b3e2-98c65b16e9f2
ms.date: 12/05/2018
ms.keywords: Enabled property [Task Scheduler], Enabled property [Task Scheduler],ITrigger interface, ITrigger interface [Task Scheduler],Enabled property, ITrigger.Enabled, ITrigger.get_Enabled, ITrigger::Enabled, ITrigger::get_Enabled, ITrigger::put_Enabled, get_Enabled, taskschd.itrigger_enabled, taskschd/ITrigger::Enabled, taskschd/ITrigger::get_Enabled, taskschd/ITrigger::put_Enabled
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
 - ITrigger::get_Enabled
 - taskschd/ITrigger::get_Enabled
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
 - ITrigger.Enabled
 - ITrigger.get_Enabled
 - ITrigger.put_Enabled
---

# ITrigger::get_Enabled


## -description

Gets or sets a Boolean value that indicates whether the trigger is enabled.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the enabled property is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-enabled-triggerbasetype-element">Enabled</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
