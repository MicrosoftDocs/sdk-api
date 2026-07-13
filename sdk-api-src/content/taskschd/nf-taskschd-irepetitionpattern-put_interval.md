---
UID: NF:taskschd.IRepetitionPattern.put_Interval
title: IRepetitionPattern::put_Interval (taskschd.h)
description: Gets or sets the amount of time between each restart of the task. (Put)
helpviewer_keywords: ["IRepetitionPattern interface [Task Scheduler]","Interval property","IRepetitionPattern.Interval","IRepetitionPattern.put_Interval","IRepetitionPattern::Interval","IRepetitionPattern::get_Interval","IRepetitionPattern::put_Interval","Interval property [Task Scheduler]","Interval property [Task Scheduler]","IRepetitionPattern interface","put_Interval","taskschd.irepetitionpattern_interval","taskschd/IRepetitionPattern::Interval","taskschd/IRepetitionPattern::get_Interval","taskschd/IRepetitionPattern::put_Interval"]
old-location: taskschd\irepetitionpattern_interval.htm
tech.root: taskschd
ms.assetid: 3ba8e4b8-c0f9-4b73-8351-b1c1b32a1e39
ms.date: 12/05/2018
ms.keywords: IRepetitionPattern interface [Task Scheduler],Interval property, IRepetitionPattern.Interval, IRepetitionPattern.put_Interval, IRepetitionPattern::Interval, IRepetitionPattern::get_Interval, IRepetitionPattern::put_Interval, Interval property [Task Scheduler], Interval property [Task Scheduler],IRepetitionPattern interface, put_Interval, taskschd.irepetitionpattern_interval, taskschd/IRepetitionPattern::Interval, taskschd/IRepetitionPattern::get_Interval, taskschd/IRepetitionPattern::put_Interval
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
 - IRepetitionPattern::put_Interval
 - taskschd/IRepetitionPattern::put_Interval
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
 - IRepetitionPattern.Interval
 - IRepetitionPattern.get_Interval
 - IRepetitionPattern.put_Interval
---

# IRepetitionPattern::put_Interval


## -description

Gets or sets the amount of time between each restart of the task.

This property is read/write.

## -parameters

## -remarks

If you specify a repetition duration for a task, you must also specify the repetition interval.

When reading or writing XML for a task, the repetition interval is specified in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-interval-repetitiontype-element">Interval</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern">IRepetitionPattern</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
