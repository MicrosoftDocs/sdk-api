---
UID: NF:taskschd.IWeeklyTrigger.get_DaysOfWeek
title: IWeeklyTrigger::get_DaysOfWeek (taskschd.h)
description: Gets or sets the days of the week in which the task runs. (Get)
helpviewer_keywords: ["DaysOfWeek property [Task Scheduler]","DaysOfWeek property [Task Scheduler]","IWeeklyTrigger interface","IWeeklyTrigger interface [Task Scheduler]","DaysOfWeek property","IWeeklyTrigger.DaysOfWeek","IWeeklyTrigger.get_DaysOfWeek","IWeeklyTrigger::DaysOfWeek","IWeeklyTrigger::get_DaysOfWeek","IWeeklyTrigger::put_DaysOfWeek","get_DaysOfWeek","taskschd.iweeklytrigger_daysofweek","taskschd/IWeeklyTrigger::DaysOfWeek","taskschd/IWeeklyTrigger::get_DaysOfWeek","taskschd/IWeeklyTrigger::put_DaysOfWeek"]
old-location: taskschd\iweeklytrigger_daysofweek.htm
tech.root: taskschd
ms.assetid: 3d4bb891-8620-401e-b1ce-39d593c1038a
ms.date: 12/05/2018
ms.keywords: DaysOfWeek property [Task Scheduler], DaysOfWeek property [Task Scheduler],IWeeklyTrigger interface, IWeeklyTrigger interface [Task Scheduler],DaysOfWeek property, IWeeklyTrigger.DaysOfWeek, IWeeklyTrigger.get_DaysOfWeek, IWeeklyTrigger::DaysOfWeek, IWeeklyTrigger::get_DaysOfWeek, IWeeklyTrigger::put_DaysOfWeek, get_DaysOfWeek, taskschd.iweeklytrigger_daysofweek, taskschd/IWeeklyTrigger::DaysOfWeek, taskschd/IWeeklyTrigger::get_DaysOfWeek, taskschd/IWeeklyTrigger::put_DaysOfWeek
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
 - IWeeklyTrigger::get_DaysOfWeek
 - taskschd/IWeeklyTrigger::get_DaysOfWeek
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
 - IWeeklyTrigger.DaysOfWeek
 - IWeeklyTrigger.get_DaysOfWeek
 - IWeeklyTrigger.put_DaysOfWeek
---

# IWeeklyTrigger::get_DaysOfWeek


## -description

Gets or sets the days of the week in which the task runs.

This property is read/write.

## -parameters

## -remarks

The following table shows the mapping of the bitwise mask used by this property.<table>
<tr>
<th>Month</th>
<th>Hex value</th>
<th>Decimal value</th>
</tr>
<tr>
<td>Sunday</td>
<td>0X01</td>
<td>1</td>
</tr>
<tr>
<td>Monday</td>
<td>0x02</td>
<td>2</td>
</tr>
<tr>
<td>Tuesday</td>
<td>0X04</td>
<td>4</td>
</tr>
<tr>
<td>Wednesday</td>
<td>0X08</td>
<td>8</td>
</tr>
<tr>
<td>Thursday</td>
<td>0X10</td>
<td>16</td>
</tr>
<tr>
<td>Friday</td>
<td>0x20</td>
<td>32</td>
</tr>
<tr>
<td>Saturday</td>
<td>0X40</td>
<td>64</td>
</tr>
</table>
 



When reading or writing your own XML for a task, the days of the week are specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-daysofweek-weeklyscheduletype-element">DaysOfWeek</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger">IWeeklyTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
