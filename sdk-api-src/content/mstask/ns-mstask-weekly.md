---
UID: NS:mstask._WEEKLY
title: WEEKLY (mstask.h)
description: Defines the interval, in weeks, between invocations of a task.
helpviewer_keywords: ["TASK_FRIDAY","TASK_MONDAY","TASK_SATURDAY","TASK_SUNDAY","TASK_THURSDAY","TASK_TUESDAY","TASK_WEDNESDAY","WEEKLY","WEEKLY structure [Task Scheduler]","_msb_weekly","mstask/WEEKLY","taskschd.weekly","triggers [Task Scheduler]","structures","WEEKLY"]
old-location: taskschd\weekly.htm
tech.root: taskschd
ms.assetid: e2c14738-846c-485e-a564-d8e738ca61a2
ms.date: 12/05/2018
ms.keywords: TASK_FRIDAY, TASK_MONDAY, TASK_SATURDAY, TASK_SUNDAY, TASK_THURSDAY, TASK_TUESDAY, TASK_WEDNESDAY, WEEKLY, WEEKLY structure [Task Scheduler], _msb_weekly, mstask/WEEKLY, taskschd.weekly, triggers [Task Scheduler],structures,WEEKLY
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
req.typenames: WEEKLY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WEEKLY
 - mstask/_WEEKLY
 - WEEKLY
 - mstask/WEEKLY
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
 - WEEKLY
---

# WEEKLY structure


## -description

Defines the interval, in weeks, between invocations of a task.

## -struct-fields

### -field WeeksInterval

Number of weeks between invocations of a task.

### -field rgfDaysOfTheWeek

Value that describes the days of the week the task runs. This value is a bitfield and is a combination of the following flags. See Remarks for an example of specifying multiple flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_SUNDAY"></a><a id="task_sunday"></a><dl>
<dt><b>TASK_SUNDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Sunday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_MONDAY"></a><a id="task_monday"></a><dl>
<dt><b>TASK_MONDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Monday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TUESDAY"></a><a id="task_tuesday"></a><dl>
<dt><b>TASK_TUESDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Tuesday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_WEDNESDAY"></a><a id="task_wednesday"></a><dl>
<dt><b>TASK_WEDNESDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Wednesday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_THURSDAY"></a><a id="task_thursday"></a><dl>
<dt><b>TASK_THURSDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Thursday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_FRIDAY"></a><a id="task_friday"></a><dl>
<dt><b>TASK_FRIDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Friday.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_SATURDAY"></a><a id="task_saturday"></a><dl>
<dt><b>TASK_SATURDAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run on Saturday.

</td>
</tr>
</table>

## -remarks

 The 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure definition.

The following C++ shows how to  combine the <b>rgfDaysOfTheWeek</b> flags. The example runs a task on every other Sunday, Wednesday, and Friday.


```cpp
WEEKLY example;
example.WeeksInterval = 2;
example.rgfDaysOfTheWeek = TASK_SUNDAY | TASK_WEDNESDAY | TASK_FRIDAY;
```

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger">IWeeklyTrigger</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>



<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval">WeeksInterval</a>