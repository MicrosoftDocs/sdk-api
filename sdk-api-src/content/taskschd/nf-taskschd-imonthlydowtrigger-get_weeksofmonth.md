---
UID: NF:taskschd.IMonthlyDOWTrigger.get_WeeksOfMonth
title: IMonthlyDOWTrigger::get_WeeksOfMonth (taskschd.h)
description: Gets or sets the weeks of the month during which the task runs. (Get)
helpviewer_keywords: ["IMonthlyDOWTrigger interface [Task Scheduler]","WeeksOfMonth property","IMonthlyDOWTrigger.WeeksOfMonth","IMonthlyDOWTrigger.get_WeeksOfMonth","IMonthlyDOWTrigger::WeeksOfMonth","IMonthlyDOWTrigger::get_WeeksOfMonth","IMonthlyDOWTrigger::put_WeeksOfMonth","WeeksOfMonth property [Task Scheduler]","WeeksOfMonth property [Task Scheduler]","IMonthlyDOWTrigger interface","get_WeeksOfMonth","taskschd.imonthlydowtrigger_weeksofmonth","taskschd/IMonthlyDOWTrigger::WeeksOfMonth","taskschd/IMonthlyDOWTrigger::get_WeeksOfMonth","taskschd/IMonthlyDOWTrigger::put_WeeksOfMonth"]
old-location: taskschd\imonthlydowtrigger_weeksofmonth.htm
tech.root: taskschd
ms.assetid: 55bbf8d6-6ff6-46a3-82e2-b5986ee3927e
ms.date: 12/05/2018
ms.keywords: IMonthlyDOWTrigger interface [Task Scheduler],WeeksOfMonth property, IMonthlyDOWTrigger.WeeksOfMonth, IMonthlyDOWTrigger.get_WeeksOfMonth, IMonthlyDOWTrigger::WeeksOfMonth, IMonthlyDOWTrigger::get_WeeksOfMonth, IMonthlyDOWTrigger::put_WeeksOfMonth, WeeksOfMonth property [Task Scheduler], WeeksOfMonth property [Task Scheduler],IMonthlyDOWTrigger interface, get_WeeksOfMonth, taskschd.imonthlydowtrigger_weeksofmonth, taskschd/IMonthlyDOWTrigger::WeeksOfMonth, taskschd/IMonthlyDOWTrigger::get_WeeksOfMonth, taskschd/IMonthlyDOWTrigger::put_WeeksOfMonth
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
 - IMonthlyDOWTrigger::get_WeeksOfMonth
 - taskschd/IMonthlyDOWTrigger::get_WeeksOfMonth
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
 - IMonthlyDOWTrigger.WeeksOfMonth
 - IMonthlyDOWTrigger.get_WeeksOfMonth
 - IMonthlyDOWTrigger.put_WeeksOfMonth
---

# IMonthlyDOWTrigger::get_WeeksOfMonth


## -description

Gets or sets the weeks of the month during which the task runs.

This property is read/write.

## -parameters

## -remarks

The following table shows the mapping of the bitwise mask used by this property. Note that you can explicitly specify the last week of the month, regardless  of what week it is, by specifying 0X10 (16).<table>
<tr>
<th>Week</th>
<th>Hex value</th>
<th>Decimal value</th>
</tr>
<tr>
<td>First</td>
<td>0X01</td>
<td>1</td>
</tr>
<tr>
<td>Second</td>
<td>0x02</td>
<td>2</td>
</tr>
<tr>
<td>Third</td>
<td>0X04</td>
<td>4</td>
</tr>
<tr>
<td>Fourth</td>
<td>0X08</td>
<td>8</td>
</tr>
<tr>
<td>Last</td>
<td>0X10</td>
<td>16</td>
</tr>
</table>
 



When reading or writing XML for a task, the weeks of the month of a monthly day-of-week calendar are specified by the <a href="/windows/desktop/TaskSchd/taskschedulerschema-weeks-monthlydayofweekscheduletype-element">Weeks</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger">IMonthlyDOWTrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
