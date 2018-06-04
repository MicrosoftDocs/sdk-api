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

# _WEEKLY structure


## -description


Defines the interval, in weeks, between invocations of a task.


## -struct-fields




### -field WeeksInterval

Number of weeks between invocations of a task.


### -field rgfDaysOfTheWeek

Value that describes the days of the week the task runs. This value is a bitfield and is a combination of the following flags. See Remarks for an example of specifying multiple flags. 



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
 


## -remarks



 The 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure definition.

The following C++ shows how to  combine the <b>rgfDaysOfTheWeek</b> flags. The example runs a task on every other Sunday, Wednesday, and Friday.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WEEKLY example;
example.WeeksInterval = 2;
example.rgfDaysOfTheWeek = TASK_SUNDAY | TASK_WEDNESDAY | TASK_FRIDAY;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c10b050a-8319-4e21-85aa-0bceb76abaaf">IWeeklyTrigger</a>



<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a>



<a href="https://msdn.microsoft.com/11f2c708-a95b-4b9c-a3a6-9b37b01d2d0b">WeeksInterval</a>
 

 

