---
UID: NF:taskschd.ITrigger.put_Id
title: ITrigger::put_Id (taskschd.h)
description: Gets or sets the identifier for the trigger. (Put)
helpviewer_keywords: ["ITrigger interface [Task Scheduler]","Id property","ITrigger.Id","ITrigger.put_Id","ITrigger::Id","ITrigger::get_Id","ITrigger::put_Id","Id property [Task Scheduler]","Id property [Task Scheduler]","ITrigger interface","put_Id","taskschd.itrigger_id","taskschd/ITrigger::Id","taskschd/ITrigger::get_Id","taskschd/ITrigger::put_Id"]
old-location: taskschd\itrigger_id.htm
tech.root: taskschd
ms.assetid: 7cf26e63-2517-44a0-9a12-06c2a903c089
ms.date: 12/05/2018
ms.keywords: ITrigger interface [Task Scheduler],Id property, ITrigger.Id, ITrigger.put_Id, ITrigger::Id, ITrigger::get_Id, ITrigger::put_Id, Id property [Task Scheduler], Id property [Task Scheduler],ITrigger interface, put_Id, taskschd.itrigger_id, taskschd/ITrigger::Id, taskschd/ITrigger::get_Id, taskschd/ITrigger::put_Id
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
 - ITrigger::put_Id
 - taskschd/ITrigger::put_Id
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
 - ITrigger.Id
 - ITrigger.get_Id
 - ITrigger.put_Id
---

# ITrigger::put_Id


## -description

Gets or sets the identifier for the trigger.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the trigger identifier is specified in the Id attribute of the individual trigger elements (for example, the Id attribute of the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-boottrigger-triggergroup-element">BootTrigger</a> element) of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
