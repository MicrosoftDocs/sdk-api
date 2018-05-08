---
UID: NF:taskschd.IMonthlyDOWTrigger.get_WeeksOfMonth
title: IMonthlyDOWTrigger::get_WeeksOfMonth
author: windows-driver-content
description: Gets or sets the weeks of the month during which the task runs.
old-location: taskschd\imonthlydowtrigger_weeksofmonth.htm
old-project: TaskSchd
ms.assetid: 55bbf8d6-6ff6-46a3-82e2-b5986ee3927e
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IMonthlyDOWTrigger interface [Task Scheduler],WeeksOfMonth property, IMonthlyDOWTrigger.WeeksOfMonth, IMonthlyDOWTrigger.get_WeeksOfMonth, IMonthlyDOWTrigger::WeeksOfMonth, IMonthlyDOWTrigger::get_WeeksOfMonth, IMonthlyDOWTrigger::put_WeeksOfMonth, WeeksOfMonth property [Task Scheduler], WeeksOfMonth property [Task Scheduler],IMonthlyDOWTrigger interface, get_WeeksOfMonth, taskschd.imonthlydowtrigger_weeksofmonth, taskschd/IMonthlyDOWTrigger::WeeksOfMonth, taskschd/IMonthlyDOWTrigger::get_WeeksOfMonth, taskschd/IMonthlyDOWTrigger::put_WeeksOfMonth
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IMonthlyDOWTrigger.WeeksOfMonth
-	IMonthlyDOWTrigger.get_WeeksOfMonth
-	IMonthlyDOWTrigger.put_WeeksOfMonth
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 



When reading or writing XML for a task, the weeks of the month of a monthly day-of-week calendar are specified by the <a href="https://msdn.microsoft.com/c126d1e2-6e60-4067-9fc2-86c9522cce5d">Weeks</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

