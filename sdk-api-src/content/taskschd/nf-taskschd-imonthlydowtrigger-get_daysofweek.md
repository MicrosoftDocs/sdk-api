---
UID: NF:taskschd.IMonthlyDOWTrigger.get_DaysOfWeek
title: IMonthlyDOWTrigger::get_DaysOfWeek (taskschd.h)
description: Gets or sets the days of the week during which the task runs. (Get)
helpviewer_keywords: ["DaysOfWeek property [Task Scheduler]","DaysOfWeek property [Task Scheduler]","IMonthlyDOWTrigger interface","IMonthlyDOWTrigger interface [Task Scheduler]","DaysOfWeek property","IMonthlyDOWTrigger.DaysOfWeek","IMonthlyDOWTrigger.get_DaysOfWeek","IMonthlyDOWTrigger::DaysOfWeek","IMonthlyDOWTrigger::get_DaysOfWeek","IMonthlyDOWTrigger::put_DaysOfWeek","get_DaysOfWeek","taskschd.imonthlydowtrigger_daysofweek","taskschd/IMonthlyDOWTrigger::DaysOfWeek","taskschd/IMonthlyDOWTrigger::get_DaysOfWeek","taskschd/IMonthlyDOWTrigger::put_DaysOfWeek"]
old-location: taskschd\imonthlydowtrigger_daysofweek.htm
tech.root: taskschd
ms.assetid: 553a0a51-fc2f-4ace-a69d-6aef4d9b06af
ms.date: 12/05/2018
ms.keywords: DaysOfWeek property [Task Scheduler], DaysOfWeek property [Task Scheduler],IMonthlyDOWTrigger interface, IMonthlyDOWTrigger interface [Task Scheduler],DaysOfWeek property, IMonthlyDOWTrigger.DaysOfWeek, IMonthlyDOWTrigger.get_DaysOfWeek, IMonthlyDOWTrigger::DaysOfWeek, IMonthlyDOWTrigger::get_DaysOfWeek, IMonthlyDOWTrigger::put_DaysOfWeek, get_DaysOfWeek, taskschd.imonthlydowtrigger_daysofweek, taskschd/IMonthlyDOWTrigger::DaysOfWeek, taskschd/IMonthlyDOWTrigger::get_DaysOfWeek, taskschd/IMonthlyDOWTrigger::put_DaysOfWeek
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
 - IMonthlyDOWTrigger::get_DaysOfWeek
 - taskschd/IMonthlyDOWTrigger::get_DaysOfWeek
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
 - IMonthlyDOWTrigger.DaysOfWeek
 - IMonthlyDOWTrigger.get_DaysOfWeek
 - IMonthlyDOWTrigger.put_DaysOfWeek
---

# IMonthlyDOWTrigger::get_DaysOfWeek


## -description

Gets or sets the days of the week during which the task runs.

This property is read/write.

## -parameters

## -remarks

The following table shows the mapping of the bitwise mask used by this property.<table>
<tr>
<th>Day of Week</th>
<th>Hex Value</th>
<th>Decimal Value</th>
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
<td>0X20</td>
<td>32</td>
</tr>
<tr>
<td>Saturday</td>
<td>0X40</td>
<td>64</td>
</tr>
</table>
 



When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the <a href="/windows/desktop/TaskSchd/taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element">DaysOfWeek</a> element.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger">IMonthlyDOWTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
