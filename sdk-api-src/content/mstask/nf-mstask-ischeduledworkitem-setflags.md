---
UID: NF:mstask.IScheduledWorkItem.SetFlags
title: IScheduledWorkItem::SetFlags (mstask.h)
description: Sets the flags that modify the behavior of any type of work item.
helpviewer_keywords: ["IScheduledWorkItem interface [Task Scheduler]","SetFlags method","IScheduledWorkItem.SetFlags","IScheduledWorkItem::SetFlags","SetFlags","SetFlags method [Task Scheduler]","SetFlags method [Task Scheduler]","IScheduledWorkItem interface","_msb_ischeduledworkitem_setflags","mstask/IScheduledWorkItem::SetFlags","taskschd.ischeduledworkitem_setflags"]
old-location: taskschd\ischeduledworkitem_setflags.htm
tech.root: taskschd
ms.assetid: 640ba3c7-ed9d-4c4c-82fd-34fc777172c2
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem interface [Task Scheduler],SetFlags method, IScheduledWorkItem.SetFlags, IScheduledWorkItem::SetFlags, SetFlags, SetFlags method [Task Scheduler], SetFlags method [Task Scheduler],IScheduledWorkItem interface, _msb_ischeduledworkitem_setflags, mstask/IScheduledWorkItem::SetFlags, taskschd.ischeduledworkitem_setflags
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
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - IScheduledWorkItem::SetFlags
 - mstask/IScheduledWorkItem::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - IScheduledWorkItem.SetFlags
---

# IScheduledWorkItem::SetFlags


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Sets the flags that modify the behavior of any type of <a href="/windows/desktop/TaskSchd/w">work item</a>.

## -parameters

### -param dwFlags

A value that specifies a combination of one or more of the following flags: 







#### TASK_FLAG_INTERACTIVE

This flag is used when converting Windows NT AT service jobs into work items. The Windows NT AT service job refers to At.exe, the Windows NT command-line utility used for creating jobs for the Windows NT Schedule service. The Task Scheduler service replaces the Schedule service and is backward compatible with it. The conversion occurs when the Task Scheduler is installed on Windows NT/Windows 2000— for example, if you install Internet Explorer 4.0, or upgrade to Windows 2000. During the setup process, the Task Scheduler installation code searches the registry for jobs created for the AT service and creates work items that will accomplish the same operation. 




For such converted jobs, the interactive flag is set if the work item is intended to be displayed to the user. When this flag is not set, no work items are displayed in the Tasks folder, and no user interface associated with the work item is presented to the user when the work item is executed.



#### TASK_FLAG_DELETE_WHEN_DONE

The work item will be deleted when there are no more scheduled run times.



#### TASK_FLAG_DISABLED

The work item is disabled. This is useful to temporarily prevent a work item from running at the scheduled time(s).



#### TASK_FLAG_HIDDEN

The work item created will be hidden.



#### TASK_FLAG_RUN_ONLY_IF_LOGGED_ON

The work item runs only if the user specified in 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setaccountinformation">IScheduledWorkItem::SetAccountInformation</a> is logged on interactively. This flag has no effect on the work items that are set to run in the local account.



#### TASK_FLAG_START_ONLY_IF_IDLE

The work item begins only if the computer is not in use at the scheduled start time.



#### TASK_FLAG_SYSTEM_REQUIRED

The work item causes the system to be resumed, or awakened, if the system is running on battery power. This flag is supported only on systems that support resume timers.



#### TASK_FLAG_KILL_ON_IDLE_END

The work item terminates if the computer makes an idle to non-idle transition while the work item is running. The computer is not considered idle until the <b>IdleWait</b> triggers' time elapses with no user input. For information regarding idle triggers, see <a href="/windows/desktop/TaskSchd/i">Idle Trigger</a>.



#### TASK_FLAG_RESTART_ON_IDLE_RESUME

The work item starts again if the computer makes a non-idle to idle transition before all the work item's <a href="/windows/desktop/TaskSchd/t">task_triggers</a> elapse. (Use this flag in conjunction with TASK_FLAG_KILL_ON_IDLE_END.)



#### TASK_FLAG_DONT_START_IF_ON_BATTERIES

The work item does not start if its target computer is running on battery power.



#### TASK_FLAG_KILL_IF_GOING_ON_BATTERIES

The work item ends, and the associated application quits if the work item's target computer switches to battery power.



#### TASK_FLAG_RUN_IF_CONNECTED_TO_INTERNET

The work item runs only if there is currently a valid Internet connection. 

<div class="alert"><b>Note</b>  This feature is currently not implemented.</div>
<div> </div>

## -returns

The 
<b>SetFlags</b> method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available.

</td>
</tr>
</table>

## -remarks

Programs must call the <b>IPersistFile::Save</b> method after calling 
<b>SetFlags</b> to update the flags.

This method is used to set those flags used by any type of scheduled work item. In contrast, 
<a href="/windows/desktop/api/mstask/nf-mstask-itask-settaskflags">ITask::SetTaskFlags</a> is used only to set flags used by scheduled tasks.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-ischeduledworkitem">IScheduledWorkItem</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-getflags">IScheduledWorkItem::GetFlags</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-setaccountinformation">IScheduledWorkItem::SetAccountInformation</a>