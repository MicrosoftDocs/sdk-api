---
UID: NS:mstask._MONTHLYDATE
title: "_MONTHLYDATE"
author: windows-sdk-content
description: Defines the day of the month the task will run.
old-location: taskschd\monthlydate.htm
old-project: taskschd
ms.assetid: 51d010c9-4e16-49b7-8034-dfb27761c6a6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MONTHLYDATE, MONTHLYDATE structure [Task Scheduler], TASK_APRIL, TASK_AUGUST, TASK_DECEMBER, TASK_FEBRUARY, TASK_JANUARY, TASK_JULY, TASK_JUNE, TASK_MARCH, TASK_MAY, TASK_NOVEMBER, TASK_OCTOBER, TASK_SEPTEMBER, _MONTHLYDATE, _msb_monthlydate, mstask/MONTHLYDATE, taskschd.monthlydate, triggers [Task Scheduler],structures,MONTHLYDATE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mstask.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MONTHLYDATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstask.h
api_name:
 - MONTHLYDATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MONTHLYDATE structure


## -description


 Defines the day of the month the task will run.


## -struct-fields




### -field rgfDays

Specifies the day of the month a task runs. This value is a bitfield that specifies the day(s) the task will run. Bit 0 corresponds to the first of the month, bit 1 to the second, and so forth.


### -field rgfMonths

Specifies the month(s) when the task runs. This value is a combination of the following flags. See Remarks for an example of setting multiple flags.

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

The following C++ example shows how to combine the flags.  The example runs a task quarterly.


```cpp
MONTHLYDATE example;
example.rgfDays = 1;
example.rgfMonths = TASK_JANUARY | TASK_APRIL | TASK_JULY | TASK_OCTOBER;
```





## -see-also




<a href="https://msdn.microsoft.com/b4716e32-7c7a-40ab-baa1-4c7ebafc3d71">TASK_TRIGGER</a>



<a href="https://msdn.microsoft.com/de50fe74-8091-4a9e-a5b9-9a8c2c684895">TRIGGER_TYPE_UNION</a>
 

 

