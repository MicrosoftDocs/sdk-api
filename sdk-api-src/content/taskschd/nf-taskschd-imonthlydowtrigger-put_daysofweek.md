---
UID: NF:taskschd.IMonthlyDOWTrigger.put_DaysOfWeek
title: IMonthlyDOWTrigger::put_DaysOfWeek (taskschd.h)
author: windows-sdk-content
description: Gets or sets the days of the week during which the task runs.
old-location: taskschd\imonthlydowtrigger_daysofweek.htm
tech.root: taskschd
ms.assetid: 553a0a51-fc2f-4ace-a69d-6aef4d9b06af
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DaysOfWeek property [Task Scheduler], DaysOfWeek property [Task Scheduler],IMonthlyDOWTrigger interface, IMonthlyDOWTrigger interface [Task Scheduler],DaysOfWeek property, IMonthlyDOWTrigger.DaysOfWeek, IMonthlyDOWTrigger.put_DaysOfWeek, IMonthlyDOWTrigger::DaysOfWeek, IMonthlyDOWTrigger::get_DaysOfWeek, IMonthlyDOWTrigger::put_DaysOfWeek, put_DaysOfWeek, taskschd.imonthlydowtrigger_daysofweek, taskschd/IMonthlyDOWTrigger::DaysOfWeek, taskschd/IMonthlyDOWTrigger::get_DaysOfWeek, taskschd/IMonthlyDOWTrigger::put_DaysOfWeek
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMonthlyDOWTrigger::put_DaysOfWeek


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
 



When reading or writing XML for a task, the days of the week of a monthly day-of-week calendar are specified by the <a href="https://msdn.microsoft.com/d84f0019-1369-465f-9054-0fb5a83cad6d">DaysOfWeek</a> element.




## -see-also




<a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

