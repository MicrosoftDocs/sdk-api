---
UID: NF:taskschd.ITaskSettings.put_Priority
title: ITaskSettings::put_Priority
author: windows-sdk-content
description: Gets or sets the priority level of the task.
old-location: taskschd\itasksettings_priority.htm
tech.root: taskschd
ms.assetid: ce6ad1bc-0d19-4a5d-b29f-8df8400f8819
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITaskSettings interface [Task Scheduler],Priority property, ITaskSettings.Priority, ITaskSettings.put_Priority, ITaskSettings::Priority, ITaskSettings::get_Priority, ITaskSettings::put_Priority, Priority property [Task Scheduler], Priority property [Task Scheduler],ITaskSettings interface, put_Priority, taskschd.itasksettings_priority, taskschd/ITaskSettings::Priority, taskschd/ITaskSettings::get_Priority, taskschd/ITaskSettings::put_Priority
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
 - ITaskSettings.Priority
 - ITaskSettings.get_Priority
 - ITaskSettings.put_Priority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

