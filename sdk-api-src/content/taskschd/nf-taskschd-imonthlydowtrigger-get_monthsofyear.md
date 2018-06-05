---
UID: NF:taskschd.IMonthlyDOWTrigger.get_MonthsOfYear
title: IMonthlyDOWTrigger::get_MonthsOfYear
author: windows-sdk-content
description: Gets or sets the months of the year during which the task runs.
old-location: taskschd\imonthlydowtrigger_monthsofyear.htm
old-project: TaskSchd
ms.assetid: cbc246cf-c577-49a5-8a4e-4b00be5c3e9d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IMonthlyDOWTrigger interface [Task Scheduler],MonthsOfYear property, IMonthlyDOWTrigger.MonthsOfYear, IMonthlyDOWTrigger.get_MonthsOfYear, IMonthlyDOWTrigger::MonthsOfYear, IMonthlyDOWTrigger::get_MonthsOfYear, IMonthlyDOWTrigger::put_MonthsOfYear, MonthsOfYear property [Task Scheduler], MonthsOfYear property [Task Scheduler],IMonthlyDOWTrigger interface, get_MonthsOfYear, taskschd.imonthlydowtrigger_monthsofyear, taskschd/IMonthlyDOWTrigger::MonthsOfYear, taskschd/IMonthlyDOWTrigger::get_MonthsOfYear, taskschd/IMonthlyDOWTrigger::put_MonthsOfYear
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IMonthlyDOWTrigger.MonthsOfYear
-	IMonthlyDOWTrigger.get_MonthsOfYear
-	IMonthlyDOWTrigger.put_MonthsOfYear
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IMonthlyDOWTrigger::get_MonthsOfYear


## -description


Gets or sets the months of the year during which the task runs.

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
<td>January</td>
<td>0X01</td>
<td>1</td>
</tr>
<tr>
<td>February</td>
<td>0x02</td>
<td>2</td>
</tr>
<tr>
<td>March</td>
<td>0X04</td>
<td>4</td>
</tr>
<tr>
<td>April</td>
<td>0X08</td>
<td>8</td>
</tr>
<tr>
<td>May</td>
<td>0X10</td>
<td>16</td>
</tr>
<tr>
<td>June</td>
<td>0X20</td>
<td>32</td>
</tr>
<tr>
<td>July</td>
<td>0x40</td>
<td>64</td>
</tr>
<tr>
<td>August</td>
<td>0X80</td>
<td>128</td>
</tr>
<tr>
<td>September</td>
<td>0X100</td>
<td>256</td>
</tr>
<tr>
<td>October</td>
<td>0X200</td>
<td>512</td>
</tr>
<tr>
<td>November</td>
<td>0X400</td>
<td>1024</td>
</tr>
<tr>
<td>December</td>
<td>0X800</td>
<td>2048</td>
</tr>
</table>
 



When reading or writing XML for a task, the months of the year of a monthly day-of-week calendar are specified by the <a href="https://msdn.microsoft.com/420fa7f4-7106-483e-9b3b-d1ba51f25222">Months</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

