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

# IMonthlyDOWTrigger::put_WeeksOfMonth


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
 

 

