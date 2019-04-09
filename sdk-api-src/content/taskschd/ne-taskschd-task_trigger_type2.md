---
UID: NE:taskschd._TASK_TRIGGER_TYPE2
title: TASK_TRIGGER_TYPE2 (taskschd.h)
author: windows-sdk-content
description: Defines the type of triggers that can be used by tasks.
old-location: taskschd\triggertype.htm
tech.root: taskschd
ms.assetid: 489015a1-5a3c-4994-aa1f-bc02dfff149d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TASK_TRIGGER_BOOT, TASK_TRIGGER_DAILY, TASK_TRIGGER_EVENT, TASK_TRIGGER_IDLE, TASK_TRIGGER_LOGON, TASK_TRIGGER_MONTHLY, TASK_TRIGGER_MONTHLYDOW, TASK_TRIGGER_REGISTRATION, TASK_TRIGGER_SESSION_STATE_CHANGE, TASK_TRIGGER_TIME, TASK_TRIGGER_TYPE2, TASK_TRIGGER_TYPE2 enumeration [Task Scheduler], TASK_TRIGGER_WEEKLY, taskschd.triggertype, taskschd/TASK_TRIGGER_BOOT, taskschd/TASK_TRIGGER_DAILY, taskschd/TASK_TRIGGER_EVENT, taskschd/TASK_TRIGGER_IDLE, taskschd/TASK_TRIGGER_LOGON, taskschd/TASK_TRIGGER_MONTHLY, taskschd/TASK_TRIGGER_MONTHLYDOW, taskschd/TASK_TRIGGER_REGISTRATION, taskschd/TASK_TRIGGER_SESSION_STATE_CHANGE, taskschd/TASK_TRIGGER_TIME, taskschd/TASK_TRIGGER_TYPE2, taskschd/TASK_TRIGGER_WEEKLY
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - taskschd.h
api_name:
 - TASK_TRIGGER_TYPE2
product: Windows
targetos: Windows
req.typenames: TASK_TRIGGER_TYPE2
req.redist: 
---

# TASK_TRIGGER_TYPE2 enumeration


## -description


Defines the type of triggers that can be used by tasks.


## -enum-fields




### -field TASK_TRIGGER_EVENT

Triggers the task when a specific event occurs. For more information about event triggers, see <a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>.


### -field TASK_TRIGGER_TIME

Triggers the task at a specific time of day. For more information about time triggers, see <a href="https://msdn.microsoft.com/4ebd5470-0801-42ff-a0c2-4d1e7f7ee365">ITimeTrigger</a>.


### -field TASK_TRIGGER_DAILY

Triggers the task on a daily schedule. For example, the task starts at a specific time every day, every other day, or every third day. For more information about daily triggers, see <a href="https://msdn.microsoft.com/9980ddb1-9873-46d2-8dea-bfc3fd78bba8">IDailyTrigger</a>.


### -field TASK_TRIGGER_WEEKLY

Triggers the task on a weekly schedule. For example, the task starts at 8:00 AM on a specific day every week or other week.  For more information about weekly triggers, see <a href="https://msdn.microsoft.com/c10b050a-8319-4e21-85aa-0bceb76abaaf">IWeeklyTrigger</a>.


### -field TASK_TRIGGER_MONTHLY

Triggers the task on a monthly schedule. For example, the task starts on specific days of specific months. For more information about monthly triggers, see <a href="https://msdn.microsoft.com/2ed206a6-22e0-4131-92ce-29536ad65c6c">IMonthlyTrigger</a>.


### -field TASK_TRIGGER_MONTHLYDOW

Triggers the task on a monthly day-of-week schedule. For example, the task starts on a specific   days of the week, weeks of the  month, and months of the year. For more information about monthly day-of-week triggers, see <a href="https://msdn.microsoft.com/a950e4a0-1fcc-4213-bdb7-d1e1cf28fe91">IMonthlyDOWTrigger</a>.


### -field TASK_TRIGGER_IDLE

Triggers the task when the computer goes into an idle state. For more information about idle triggers, see <a href="https://msdn.microsoft.com/aca5305f-68fc-4211-9f71-3f572340e94d">IIdleTrigger</a>.


### -field TASK_TRIGGER_REGISTRATION

Triggers the task when the task is registered. For more information about registration triggers, see <a href="https://msdn.microsoft.com/0862f7ac-69d6-4271-8d39-c5bd7038a95e">IRegistrationTrigger</a>.


### -field TASK_TRIGGER_BOOT

Triggers the task when the computer boots.  For more information about boot triggers, see <a href="https://msdn.microsoft.com/8f186ee2-8d74-426c-9173-523a335422c9">IBootTrigger</a>.


### -field TASK_TRIGGER_LOGON

Triggers the task when a specific user logs on.  For more information about logon triggers, see <a href="https://msdn.microsoft.com/c0206a18-53f2-4def-8f54-2b175a0579f4">ILogonTrigger</a>.


### -field TASK_TRIGGER_SESSION_STATE_CHANGE

Triggers the task when a specific user session state changes.  For more information about session state change triggers, see <a href="https://msdn.microsoft.com/0bf56d67-6c44-4978-93a9-7b525f2bf140">ISessionStateChangeTrigger</a>.


### -field TASK_TRIGGER_CUSTOM_TRIGGER_01




## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/9779d32b-0142-41bb-88e2-df79a3b0c1b2">Task Scheduler Enumerated Types</a>
 

 

