---
UID: NF:taskschd.ITriggerCollection.Create
title: ITriggerCollection::Create
author: windows-driver-content
description: Creates a new trigger for the task.
old-location: taskschd\itriggercollection_create.htm
old-project: TaskSchd
ms.assetid: 70780fca-ba97-42b8-bc00-867c2761953c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Create, Create method [Task Scheduler], Create method [Task Scheduler],ITriggerCollection interface, ITriggerCollection interface [Task Scheduler],Create method, ITriggerCollection.Create, ITriggerCollection::Create, TASK_TRIGGER_BOOT, TASK_TRIGGER_DAILY, TASK_TRIGGER_EVENT, TASK_TRIGGER_IDLE, TASK_TRIGGER_LOGON, TASK_TRIGGER_MONTHLY, TASK_TRIGGER_MONTHLYDOW, TASK_TRIGGER_REGISTRATION, TASK_TRIGGER_SESSION_STATE_CHANGE, TASK_TRIGGER_TIME, TASK_TRIGGER_WEEKLY, taskschd.itriggercollection_create, taskschd/ITriggerCollection::Create, triggers [Task Scheduler],creating
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
-	ITriggerCollection.Create
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITriggerCollection::Create


## -description


Creates a new trigger for the task.


## -parameters




### -param type [in]

This parameter is set to one of the following  <a href="https://msdn.microsoft.com/489015a1-5a3c-4994-aa1f-bc02dfff149d">TASK_TRIGGER_TYPE2</a> enumeration constants.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_EVENT"></a><a id="task_trigger_event"></a><dl>
<dt><b>TASK_TRIGGER_EVENT</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Triggers the task when a specific event occurs.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_TIME"></a><a id="task_trigger_time"></a><dl>
<dt><b>TASK_TRIGGER_TIME</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Triggers the task at a specific time of day.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_DAILY"></a><a id="task_trigger_daily"></a><dl>
<dt><b>TASK_TRIGGER_DAILY</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Triggers the task on a daily schedule. For example, the task starts at a specific time every day, every-other day, every third day, and so on.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_WEEKLY"></a><a id="task_trigger_weekly"></a><dl>
<dt><b>TASK_TRIGGER_WEEKLY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Triggers the task on a weekly schedule. For example, the task starts at 8:00 AM on a specific day every week or other week.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_MONTHLY"></a><a id="task_trigger_monthly"></a><dl>
<dt><b>TASK_TRIGGER_MONTHLY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Triggers the task on a monthly schedule. For example, the task starts on specific days of specific months.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_MONTHLYDOW"></a><a id="task_trigger_monthlydow"></a><dl>
<dt><b>TASK_TRIGGER_MONTHLYDOW</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Triggers the task on a monthly day-of-week schedule. For example, the task starts on a specific   days of the week, weeks of the  month, and months of the year.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_IDLE"></a><a id="task_trigger_idle"></a><dl>
<dt><b>TASK_TRIGGER_IDLE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
Triggers the task when the computer goes into an idle state.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_REGISTRATION"></a><a id="task_trigger_registration"></a><dl>
<dt><b>TASK_TRIGGER_REGISTRATION</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
Triggers the task when the task is registered.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_BOOT"></a><a id="task_trigger_boot"></a><dl>
<dt><b>TASK_TRIGGER_BOOT</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
Triggers the task when the computer boots.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_LOGON"></a><a id="task_trigger_logon"></a><dl>
<dt><b>TASK_TRIGGER_LOGON</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
Triggers the task when a specific user logs on.

</td>
</tr>
<tr>
<td width="40%"><a id="TASK_TRIGGER_SESSION_STATE_CHANGE"></a><a id="task_trigger_session_state_change"></a><dl>
<dt><b>TASK_TRIGGER_SESSION_STATE_CHANGE</b></dt>
<dt>11</dt>
</dl>
</td>
<td width="60%">
Triggers the task when a specific session state changes.

</td>
</tr>
</table>
 


### -param ppTrigger [out]

An <a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a> interface that represents the new trigger.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

