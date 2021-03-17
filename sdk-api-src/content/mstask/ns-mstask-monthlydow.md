---
UID: NS:mstask._MONTHLYDOW
title: MONTHLYDOW (mstask.h)
description: Defines the date(s) that the task runs by month, week, and day of the week.
helpviewer_keywords: ["MONTHLYDOW","MONTHLYDOW structure [Task Scheduler]","TASK_APRIL","TASK_AUGUST","TASK_DECEMBER","TASK_FEBRUARY","TASK_FIRST_WEEK","TASK_FOURTH_WEEK","TASK_FRIDAY","TASK_JANUARY","TASK_JULY","TASK_JUNE","TASK_LAST_WEEK","TASK_MARCH","TASK_MAY","TASK_MONDAY","TASK_NOVEMBER","TASK_OCTOBER","TASK_SATURDAY","TASK_SECOND_WEEK","TASK_SEPTEMBER","TASK_SUNDAY","TASK_THIRD_WEEK","TASK_THURSDAY","TASK_TUESDAY","TASK_WEDNESDAY","_msb_monthlydow","mstask/MONTHLYDOW","taskschd.monthlydow","triggers [Task Scheduler]","structures","MONTHLYDOW"]
old-location: taskschd\monthlydow.htm
tech.root: taskschd
ms.assetid: 1f353611-0542-4534-91bf-4a76f41c9c9d
ms.date: 12/05/2018
ms.keywords: MONTHLYDOW, MONTHLYDOW structure [Task Scheduler], TASK_APRIL, TASK_AUGUST, TASK_DECEMBER, TASK_FEBRUARY, TASK_FIRST_WEEK, TASK_FOURTH_WEEK, TASK_FRIDAY, TASK_JANUARY, TASK_JULY, TASK_JUNE, TASK_LAST_WEEK, TASK_MARCH, TASK_MAY, TASK_MONDAY, TASK_NOVEMBER, TASK_OCTOBER, TASK_SATURDAY, TASK_SECOND_WEEK, TASK_SEPTEMBER, TASK_SUNDAY, TASK_THIRD_WEEK, TASK_THURSDAY, TASK_TUESDAY, TASK_WEDNESDAY, _msb_monthlydow, mstask/MONTHLYDOW, taskschd.monthlydow, triggers [Task Scheduler],structures,MONTHLYDOW
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
req.typenames: MONTHLYDOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MONTHLYDOW
 - mstask/_MONTHLYDOW
 - MONTHLYDOW
 - mstask/MONTHLYDOW
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
 - MONTHLYDOW
---

# MONTHLYDOW structure


## -description

 Defines the date(s) that the task runs by month, week, and day of the week.

## -struct-fields

### -field wWhichWeek

Specifies the week of the month when the task runs. This value is exclusive and is one of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_FIRST_WEEK"></a><a id="task_first_week"></a><dl>
<dt><b>TASK_FIRST_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the first and seventh day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_SECOND_WEEK"></a><a id="task_second_week"></a><dl>
<dt><b>TASK_SECOND_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the eighth and 14<sup>th</sup> day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_THIRD_WEEK"></a><a id="task_third_week"></a><dl>
<dt><b>TASK_THIRD_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the 15<sup>th</sup> and 21<sup>st</sup> day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_FOURTH_WEEK"></a><a id="task_fourth_week"></a><dl>
<dt><b>TASK_FOURTH_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the 22<sup>nd</sup> and 28<sup>th</sup> of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LAST_WEEK"></a><a id="task_last_week"></a><dl>
<dt><b>TASK_LAST_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the last seven days of the month.

</td>
</tr>
</table>

### -field rgfDaysOfTheWeek

Specifies the day(s) of the week (specified in <b>wWhichWeek</b>) when the task runs. This value is a combination of the following flags. 



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

### -field rgfMonths

Value that describes the month(s) when the task runs. This value is a combination of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_JANUARY"></a><a id="task_january"></a><dl>
<dt><b>TASK_JANUARY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in January.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_FEBRUARY"></a><a id="task_february"></a><dl>
<dt><b>TASK_FEBRUARY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in February.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_MARCH"></a><a id="task_march"></a><dl>
<dt><b>TASK_MARCH</b></dt>
</dl>
</td>
<td width="60%">
The task will run in March.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_APRIL"></a><a id="task_april"></a><dl>
<dt><b>TASK_APRIL</b></dt>
</dl>
</td>
<td width="60%">
The task will run in April.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_MAY"></a><a id="task_may"></a><dl>
<dt><b>TASK_MAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in May.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_JUNE"></a><a id="task_june"></a><dl>
<dt><b>TASK_JUNE</b></dt>
</dl>
</td>
<td width="60%">
The task will run in June.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_JULY"></a><a id="task_july"></a><dl>
<dt><b>TASK_JULY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in July.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_AUGUST"></a><a id="task_august"></a><dl>
<dt><b>TASK_AUGUST</b></dt>
</dl>
</td>
<td width="60%">
The task will run in August.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_SEPTEMBER"></a><a id="task_september"></a><dl>
<dt><b>TASK_SEPTEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in September.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_OCTOBER"></a><a id="task_october"></a><dl>
<dt><b>TASK_OCTOBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in October.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_NOVEMBER"></a><a id="task_november"></a><dl>
<dt><b>TASK_NOVEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in November.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_DECEMBER"></a><a id="task_december"></a><dl>
<dt><b>TASK_DECEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in December.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure definition.

The following C++ example shows how to  combine these flags. The example runs a task on the Monday and the Friday of the third week of every third month.


```cpp
MONTHLYDOW example;
example.wWhichWeek = TASK_THIRD_WEEK;
example.rgfDaysOfTheWeek = TASK_FRIDAY | TASK_MONDAY;
example.rgfMonths = TASK_JANUARY | TASK_APRIL | TASK_JULY | TASK_OCTOBER;
```

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger">IMonthlyDOWTrigger</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>



<a href="/windows/desktop/api/mstask/ns-mstask-trigger_type_union">TRIGGER_TYPE_UNION</a>