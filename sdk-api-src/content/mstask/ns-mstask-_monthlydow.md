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

# _MONTHLYDOW structure


## -description


 Defines the date(s) that the task runs by month, week, and day of the week.


## -struct-fields




### -field wWhichWeek

Specifies the week of the month when the task runs. This value is exclusive and is one of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_FIRST_WEEK"></a><a id="task_first_week"></a><dl>
<dt><b>TASK_FIRST_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the first and seventh day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_SECOND_WEEK"></a><a id="task_second_week"></a><dl>
<dt><b>TASK_SECOND_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the eighth and 14<sup>th</sup> day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_THIRD_WEEK"></a><a id="task_third_week"></a><dl>
<dt><b>TASK_THIRD_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the 15<sup>th</sup> and 21<sup>st</sup> day of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_FOURTH_WEEK"></a><a id="task_fourth_week"></a><dl>
<dt><b>TASK_FOURTH_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the 22<sup>nd</sup> and 28<sup>th</sup> of the month.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_LAST_WEEK"></a><a id="task_last_week"></a><dl>
<dt><b>TASK_LAST_WEEK</b></dt>
</dl>
</td>
<td width="60%">
The task will run between the last seven days of the month.

</td>
</tr>
</table>
 


### -field rgfDaysOfTheWeek

Specifies the day(s) of the week (specified in <b>wWhichWeek</b>) when the task runs. This value is a combination of the following flags. 



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
 


### -field rgfMonths

Value that describes the month(s) when the task runs. This value is a combination of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_JANUARY"></a><a id="task_january"></a><dl>
<dt><b>TASK_JANUARY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in January.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_FEBRUARY"></a><a id="task_february"></a><dl>
<dt><b>TASK_FEBRUARY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in February.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_MARCH"></a><a id="task_march"></a><dl>
<dt><b>TASK_MARCH</b></dt>
</dl>
</td>
<td width="60%">
The task will run in March.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_APRIL"></a><a id="task_april"></a><dl>
<dt><b>TASK_APRIL</b></dt>
</dl>
</td>
<td width="60%">
The task will run in April.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_MAY"></a><a id="task_may"></a><dl>
<dt><b>TASK_MAY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in May.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_JUNE"></a><a id="task_june"></a><dl>
<dt><b>TASK_JUNE</b></dt>
</dl>
</td>
<td width="60%">
The task will run in June.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_JULY"></a><a id="task_july"></a><dl>
<dt><b>TASK_JULY</b></dt>
</dl>
</td>
<td width="60%">
The task will run in July.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_AUGUST"></a><a id="task_august"></a><dl>
<dt><b>TASK_AUGUST</b></dt>
</dl>
</td>
<td width="60%">
The task will run in August.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_SEPTEMBER"></a><a id="task_september"></a><dl>
<dt><b>TASK_SEPTEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in September.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_OCTOBER"></a><a id="task_october"></a><dl>
<dt><b>TASK_OCTOBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in October.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_NOVEMBER"></a><a id="task_november"></a><dl>
<dt><b>TASK_NOVEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in November.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_DECEMBER"></a><a id="task_december"></a><dl>
<dt><b>TASK_DECEMBER</b></dt>
</dl>
</td>
<td width="60%">
The task will run in December.

</td>
</tr>
</table>
 


## -remarks



The 
<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a> union uses an instance of this structure as part of the <b>Type</b> member of the 
<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a> structure definition.

The following C++ example shows how to  combine these flags. The example runs a task on the Monday and the Friday of the third week of every third month.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>MONTHLYDOW example;
example.wWhichWeek = TASK_THIRD_WEEK;
example.rgfDaysOfTheWeek = TASK_FRIDAY | TASK_MONDAY;
example.rgfMonths = TASK_JANUARY | TASK_APRIL | TASK_JULY | TASK_OCTOBER;</pre>
</td>
</tr>
</table></span></div>





## -see-also




<a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>



<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a>
 

 

