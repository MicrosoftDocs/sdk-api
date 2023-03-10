---
UID: NF:taskschd.IRepetitionPattern.put_StopAtDurationEnd
title: IRepetitionPattern::put_StopAtDurationEnd (taskschd.h)
description: Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration. (Put)
helpviewer_keywords: ["IRepetitionPattern interface [Task Scheduler]","StopAtDurationEnd property","IRepetitionPattern.StopAtDurationEnd","IRepetitionPattern.put_StopAtDurationEnd","IRepetitionPattern::StopAtDurationEnd","IRepetitionPattern::get_StopAtDurationEnd","IRepetitionPattern::put_StopAtDurationEnd","StopAtDurationEnd property [Task Scheduler]","StopAtDurationEnd property [Task Scheduler]","IRepetitionPattern interface","put_StopAtDurationEnd","taskschd.irepetitionpattern_stopatdurationend","taskschd/IRepetitionPattern::StopAtDurationEnd","taskschd/IRepetitionPattern::get_StopAtDurationEnd","taskschd/IRepetitionPattern::put_StopAtDurationEnd"]
old-location: taskschd\irepetitionpattern_stopatdurationend.htm
tech.root: taskschd
ms.assetid: a43b5b32-a496-4f59-89f2-4b8566332e03
ms.date: 12/05/2018
ms.keywords: IRepetitionPattern interface [Task Scheduler],StopAtDurationEnd property, IRepetitionPattern.StopAtDurationEnd, IRepetitionPattern.put_StopAtDurationEnd, IRepetitionPattern::StopAtDurationEnd, IRepetitionPattern::get_StopAtDurationEnd, IRepetitionPattern::put_StopAtDurationEnd, StopAtDurationEnd property [Task Scheduler], StopAtDurationEnd property [Task Scheduler],IRepetitionPattern interface, put_StopAtDurationEnd, taskschd.irepetitionpattern_stopatdurationend, taskschd/IRepetitionPattern::StopAtDurationEnd, taskschd/IRepetitionPattern::get_StopAtDurationEnd, taskschd/IRepetitionPattern::put_StopAtDurationEnd
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
 - IRepetitionPattern::put_StopAtDurationEnd
 - taskschd/IRepetitionPattern::put_StopAtDurationEnd
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
 - IRepetitionPattern.StopAtDurationEnd
 - IRepetitionPattern.get_StopAtDurationEnd
 - IRepetitionPattern.put_StopAtDurationEnd
---

# IRepetitionPattern::put_StopAtDurationEnd


## -description

Gets or sets a Boolean value that indicates if  a running instance of the task is stopped at the end of the repetition pattern duration.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, this information is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-stopatdurationend-repetitiontype-element">StopAtDurationEnd</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern">IRepetitionPattern</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
