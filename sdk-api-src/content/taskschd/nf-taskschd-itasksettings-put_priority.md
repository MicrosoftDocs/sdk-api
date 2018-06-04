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

# ITaskSettings::put_Priority


## -description


Gets or sets the priority level of the task.

This property is read/write.


## -parameters


## -remarks



Priority level 0 is the highest priority, and priority level 10 is the lowest priority. The default value is 7. Priority levels 7 and 8 are used for background tasks, and priority levels 4, 5, and 6 are used for interactive tasks.

The task's action is started in a process with a priority that is based on a Priority Class value. A Priority Level value (thread priority) is used for COM handler, message box, and email task actions. For more information about the Priority Class and Priority Level values, see <a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>. The following table lists the possible values for the <i>priority</i> parameter, and the corresponding Priority Class and Priority Level values.

<table>
<tr>
<th>Task <i>priority</i></th>
<th>Priority Class</th>
<th>Priority Level</th>
</tr>
<tr>
<td>0</td>
<td>REALTIME_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
</tr>
<tr>
<td>1</td>
<td>HIGH_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_HIGHEST</td>
</tr>
<tr>
<td>2</td>
<td>ABOVE_NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
</tr>
<tr>
<td>3</td>
<td>ABOVE_NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
</tr>
<tr>
<td>4</td>
<td>NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_NORMAL</td>
</tr>
<tr>
<td>5</td>
<td>NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_NORMAL</td>
</tr>
<tr>
<td>6</td>
<td>NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_NORMAL</td>
</tr>
<tr>
<td>7</td>
<td>BELOW_NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
</tr>
<tr>
<td>8</td>
<td>BELOW_NORMAL_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
</tr>
<tr>
<td>9</td>
<td>IDLE_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_LOWEST</td>
</tr>
<tr>
<td>10</td>
<td>IDLE_PRIORITY_CLASS</td>
<td>THREAD_PRIORITY_IDLE</td>
</tr>
</table>
 

When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/4885fffa-b7d9-4f5e-b6e8-6f18b01c2427">Priority (settingsType)</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>
 

 

