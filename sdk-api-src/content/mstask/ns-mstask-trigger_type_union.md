---
UID: NS:mstask._TRIGGER_TYPE_UNION
title: TRIGGER_TYPE_UNION (mstask.h)
description: Defines the invocation schedule of the trigger within the Type member of a TASK_TRIGGER structure.
helpviewer_keywords: ["TRIGGER_TYPE_UNION","TRIGGER_TYPE_UNION union [Task Scheduler]","_msb_trigger_type_union","mstask/TRIGGER_TYPE_UNION","taskschd.trigger_type_union"]
old-location: taskschd\trigger_type_union.htm
tech.root: taskschd
ms.assetid: de50fe74-8091-4a9e-a5b9-9a8c2c684895
ms.date: 12/05/2018
ms.keywords: TRIGGER_TYPE_UNION, TRIGGER_TYPE_UNION union [Task Scheduler], _msb_trigger_type_union, mstask/TRIGGER_TYPE_UNION, taskschd.trigger_type_union
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRIGGER_TYPE_UNION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRIGGER_TYPE_UNION
 - mstask/_TRIGGER_TYPE_UNION
 - TRIGGER_TYPE_UNION
 - mstask/TRIGGER_TYPE_UNION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstask.h
api_name:
 - TRIGGER_TYPE_UNION
---

# TRIGGER_TYPE_UNION structure


## -description

Defines the invocation schedule of the trigger within the <b>Type</b> member of a 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure.

## -struct-fields

### -field Daily

A 
<a href="/windows/desktop/api/mstask/ns-mstask-daily">DAILY</a> structure that specifies the number of days between invocations of a task.

### -field Weekly

A 
<a href="/windows/desktop/api/mstask/ns-mstask-weekly">WEEKLY</a> structure that specifies the number of weeks between invocations of a task, and day(s) of the week the task will run.

### -field MonthlyDate

A 
<a href="/windows/desktop/api/mstask/ns-mstask-monthlydate">MONTHLYDATE</a> structure that specifies the month(s) and day(s) of the month a task will run.

### -field MonthlyDOW

A 
<a href="/windows/desktop/api/mstask/ns-mstask-monthlydow">MONTHLYDOW</a> structure that specifies the day(s) of the year a task runs by month(s), week of month, and day(s) of week.

## -remarks

The <b>TriggerType</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure defines which fields of this union are used.

## -see-also

<a href="/windows/desktop/api/mstask/ns-mstask-daily">DAILY</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/api/mstask/ns-mstask-monthlydate">MONTHLYDATE</a>



<a href="/windows/desktop/api/mstask/ns-mstask-monthlydow">MONTHLYDOW</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type">Type</a>



<a href="/windows/desktop/api/mstask/ns-mstask-weekly">WEEKLY</a>