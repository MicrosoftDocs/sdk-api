---
UID: NF:taskschd.IRepetitionPattern.put_Duration
title: IRepetitionPattern::put_Duration (taskschd.h)
description: Gets or sets how long the pattern is repeated. (Put)
helpviewer_keywords: ["Duration property [Task Scheduler]","Duration property [Task Scheduler]","IRepetitionPattern interface","IRepetitionPattern interface [Task Scheduler]","Duration property","IRepetitionPattern.Duration","IRepetitionPattern.put_Duration","IRepetitionPattern::Duration","IRepetitionPattern::get_Duration","IRepetitionPattern::put_Duration","put_Duration","taskschd.irepetitionpattern_duration","taskschd/IRepetitionPattern::Duration","taskschd/IRepetitionPattern::get_Duration","taskschd/IRepetitionPattern::put_Duration"]
old-location: taskschd\irepetitionpattern_duration.htm
tech.root: taskschd
ms.assetid: 86deb09e-d6ad-4a8d-9fdf-e3bc5ee73b1f
ms.date: 12/05/2018
ms.keywords: Duration property [Task Scheduler], Duration property [Task Scheduler],IRepetitionPattern interface, IRepetitionPattern interface [Task Scheduler],Duration property, IRepetitionPattern.Duration, IRepetitionPattern.put_Duration, IRepetitionPattern::Duration, IRepetitionPattern::get_Duration, IRepetitionPattern::put_Duration, put_Duration, taskschd.irepetitionpattern_duration, taskschd/IRepetitionPattern::Duration, taskschd/IRepetitionPattern::get_Duration, taskschd/IRepetitionPattern::put_Duration
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
 - IRepetitionPattern::put_Duration
 - taskschd/IRepetitionPattern::put_Duration
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
 - IRepetitionPattern.Duration
 - IRepetitionPattern.get_Duration
 - IRepetitionPattern.put_Duration
---

# IRepetitionPattern::put_Duration


## -description

Gets or sets how long the pattern is repeated.

This property is read/write.

## -parameters

## -remarks

If you specify a repetition duration for a task, you must also specify the repetition interval.

When reading or writing XML for a task, the repetition duration is specified in the  <a href="/windows/desktop/TaskSchd/taskschedulerschema-duration-repetitiontype-element">Duration</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern">IRepetitionPattern</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
