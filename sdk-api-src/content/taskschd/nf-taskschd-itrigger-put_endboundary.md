---
UID: NF:taskschd.ITrigger.put_EndBoundary
title: ITrigger::put_EndBoundary (taskschd.h)
description: Gets or sets the date and time when the trigger is deactivated. (Put)
helpviewer_keywords: ["EndBoundary property [Task Scheduler]","EndBoundary property [Task Scheduler]","ITrigger interface","ITrigger interface [Task Scheduler]","EndBoundary property","ITrigger.EndBoundary","ITrigger.put_EndBoundary","ITrigger::EndBoundary","ITrigger::get_EndBoundary","ITrigger::put_EndBoundary","put_EndBoundary","taskschd.itrigger_endboundary","taskschd/ITrigger::EndBoundary","taskschd/ITrigger::get_EndBoundary","taskschd/ITrigger::put_EndBoundary"]
old-location: taskschd\itrigger_endboundary.htm
tech.root: taskschd
ms.assetid: 985316de-eaba-478f-a53f-1bea2a0cc9c6
ms.date: 12/05/2018
ms.keywords: EndBoundary property [Task Scheduler], EndBoundary property [Task Scheduler],ITrigger interface, ITrigger interface [Task Scheduler],EndBoundary property, ITrigger.EndBoundary, ITrigger.put_EndBoundary, ITrigger::EndBoundary, ITrigger::get_EndBoundary, ITrigger::put_EndBoundary, put_EndBoundary, taskschd.itrigger_endboundary, taskschd/ITrigger::EndBoundary, taskschd/ITrigger::get_EndBoundary, taskschd/ITrigger::put_EndBoundary
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITrigger::put_EndBoundary
 - taskschd/ITrigger::put_EndBoundary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITrigger.EndBoundary
 - ITrigger.get_EndBoundary
 - ITrigger.put_EndBoundary
---

# ITrigger::put_EndBoundary


## -description

Gets or sets the date and time when the trigger is deactivated.

The trigger cannot start the task after it is deactivated.

This property is read/write.

## -parameters

## -remarks

The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM. The (+-)HH:MM section of the format defines a certain number of hours and minutes ahead or behind Coordinated Universal Time (UTC). For example the date October 11th, 2005 at 1:21:17 with an offset of eight hours behind UTC would be written as 2005-10-11T13:21:17-08:00. If Z is specified for the UTC offset (for example, 2005-10-11T13:21:17Z), then the no offset from UTC will be used. If you do not specify any offset time or Z for the offset (for example, 2005-10-11T13:21:17), then the time zone and daylight saving information that is set on the local computer will be used.  When an offset is specified (using hours and minutes or Z), then the time and offset are always used regardless of the time zone and daylight saving settings on the local computer.

When reading or writing XML for a task, the trigger end boundary is specified in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-endboundary-triggerbasetype-element">EndBoundary</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
