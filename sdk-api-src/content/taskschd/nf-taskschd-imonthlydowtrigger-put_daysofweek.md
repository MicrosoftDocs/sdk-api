---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

