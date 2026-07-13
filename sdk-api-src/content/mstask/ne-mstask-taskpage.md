---
UID: NE:mstask._TASKPAGE
title: TASKPAGE (mstask.h)
description: Defines the type of task page to be retrieved.
helpviewer_keywords: ["TASKPAGE","TASKPAGE enumeration [Task Scheduler]","TASKPAGE_SCHEDULE","TASKPAGE_SETTINGS","TASKPAGE_TASK","_msb_taskpage","mstask/TASKPAGE","mstask/TASKPAGE_SCHEDULE","mstask/TASKPAGE_SETTINGS","mstask/TASKPAGE_TASK","task page [Task Scheduler]","enumerations","TASKPAGE","taskschd.taskpage"]
old-location: taskschd\taskpage.htm
tech.root: taskschd
ms.assetid: 6c822d4c-9d42-48a2-b378-06670acc39cf
ms.date: 12/05/2018
ms.keywords: TASKPAGE, TASKPAGE enumeration [Task Scheduler], TASKPAGE_SCHEDULE, TASKPAGE_SETTINGS, TASKPAGE_TASK, _msb_taskpage, mstask/TASKPAGE, mstask/TASKPAGE_SCHEDULE, mstask/TASKPAGE_SETTINGS, mstask/TASKPAGE_TASK, task page [Task Scheduler],enumerations,TASKPAGE, taskschd.taskpage
req.header: mstask.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TASKPAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TASKPAGE
 - mstask/_TASKPAGE
 - TASKPAGE
 - mstask/TASKPAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mstask.h
api_name:
 - TASKPAGE
---

# TASKPAGE enumeration


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-enumerated-types">Task Scheduler 2.0 Enumerated Types</a> instead.] ]

Defines the type of task page to be retrieved.

Each property page can be used to define the properties of a <a href="/windows/desktop/TaskSchd/t">task object</a>.

## -enum-fields

### -field TASKPAGE_TASK:0

Specifies the Task page for the task. This page provides the following UI elements: 




<ul>
<li>
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-run">Run</a>: This field specifies the name of the application associated with the task.</li>
<li>This property can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-itask-setapplicationname">ITask::SetApplicationName</a>.</li>
<li><b>Start in</b>: This field specifies the <a href="/windows/desktop/TaskSchd/w">working directory</a> for the task.</li>
<li>This property can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-itask-setworkingdirectory">ITask::SetWorkingDirectory</a>.</li>
<li><b>Comments</b>: This field specifies any application-defined comments for the task.</li>
<li>This property can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcomment">IScheduledWorkItem::SetComment</a>.</li>
<li><b>Run as</b>: (Windows Server 2003, Windows XP, and  Windows 2000 only.) This field specifies the account name under which the task will run. To the right of this field is a <b>Password</b> button for specifying the password for the account.</li>
<li>This property can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setaccountinformation">IScheduledWorkItem::SetAccountInformation</a>.</li>
<li><b>Enabled</b> (scheduled task runs at specific time): This checkbox specifies whether the TASK_TRIGGER_FLAG_DISABLED flag is set.</li>
<li>This property can also be set by setting this flag in the <b>rgFlags</b> member of the 
<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a> structure.</li>
</ul>

### -field TASKPAGE_SCHEDULE:1

Specifies the Schedule page for the task. This page is used to manage the <a href="/windows/desktop/TaskSchd/t">triggers</a> for the task. The user can create triggers, edit triggers, and delete triggers from this page. 




This page provides the following UI elements:

<ul>
<li><b>Trigger</b> list box: This list box is displayed only if multiple triggers exist.</li>
<li><b>Schedule Task</b>: This field specifies how often the task will run: daily, weekly, monthly, once, at system startup, at logon, or when idle.</li>
<li><b>Start Time</b>: This field specifies the time of day the task will run.</li>
<li><b>Advanced</b>: This button allows you to set the start date and end date for running the task.</li>
<li><b>Schedule Task</b> group box: This group box is only displayed if the <b>Schedule Task</b> field specifies daily, weekly, monthly, or once.</li>
<li><b>Show multiple schedules</b>: Shows all triggers. When checked, Trigger list box is displayed.</li>
</ul>

### -field TASKPAGE_SETTINGS:2

Specifies the Settings page for the task. The user can specify what happens when the task is completed, <a href="/windows/desktop/TaskSchd/i">idle conditions</a>, and power management properties for the task. 




This page provides the following UI elements:

<ul>
<li><b>Scheduled Task Completed</b> group box: This group box includes check boxes for setting the TASK_FLAG_DELETE_WHEN_DONE flag and the maximum run time for the task.</li>
<li>The TASK_FLAG_DELETE_WHEN_DONE flag can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>. The maximum run time can be set by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-itask-setmaxruntime">ITask::SetMaxRunTime</a>.</li>
<li><b>Idle Time</b> group box: This group box includes fields for setting idle conditions.</li>
<li>The idle time can also be set programmatically by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setidlewait">IScheduledWorkItem::SetIdleWait</a>. The TASK_FLAG_START_ONLY_IF_IDLE and TASK_FLAG_KILL_ON_IDLE_END flags can be set by calling 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>.</li>
<li><b>Power management</b> group box: (Windows 95 only) This group box includes check boxes for indicating how the task behaves when the system is losing power.</li>
<li>These properties can also be set programmatically by setting the TASK_FLAG_DONT_START_IF_ON_BATTERIES and TASK_FLAG_KILL_IF_GOING_ON_BATTERIES flags using 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-iprovidetaskpage-getpage">IProvideTaskPage::GetPage</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setaccountinformation">IScheduledWorkItem::SetAccountInformation</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setcomment">IScheduledWorkItem::SetComment</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setflags">IScheduledWorkItem::SetFlags</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setidlewait">IScheduledWorkItem::SetIdleWait</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setapplicationname">ITask::SetApplicationName</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setmaxruntime">ITask::SetMaxRunTime</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itask-setworkingdirectory">ITask::SetWorkingDirectory</a>



<a href="/windows/desktop/api/mstask/ns-mstask-task_trigger">TASK_TRIGGER</a>
