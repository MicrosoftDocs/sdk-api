---
UID: NF:taskschd.IWeeklyTrigger.get_DaysOfWeek
title: IWeeklyTrigger::get_DaysOfWeek
author: windows-sdk-content
description: Gets or sets the days of the week in which the task runs.
old-location: taskschd\iweeklytrigger_daysofweek.htm
old-project: TaskSchd
ms.assetid: 3d4bb891-8620-401e-b1ce-39d593c1038a
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: DaysOfWeek property [Task Scheduler], DaysOfWeek property [Task Scheduler],IWeeklyTrigger interface, IWeeklyTrigger interface [Task Scheduler],DaysOfWeek property, IWeeklyTrigger.DaysOfWeek, IWeeklyTrigger.get_DaysOfWeek, IWeeklyTrigger::DaysOfWeek, IWeeklyTrigger::get_DaysOfWeek, IWeeklyTrigger::put_DaysOfWeek, get_DaysOfWeek, taskschd.iweeklytrigger_daysofweek, taskschd/IWeeklyTrigger::DaysOfWeek, taskschd/IWeeklyTrigger::get_DaysOfWeek, taskschd/IWeeklyTrigger::put_DaysOfWeek
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IWeeklyTrigger.DaysOfWeek
-	IWeeklyTrigger.get_DaysOfWeek
-	IWeeklyTrigger.put_DaysOfWeek
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 



When reading or writing your own XML for a task, the days of the week are specified using the <a href="https://msdn.microsoft.com/86555681-2324-4095-9eab-fdef40e0acba">DaysOfWeek</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/c10b050a-8319-4e21-85aa-0bceb76abaaf">IWeeklyTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

