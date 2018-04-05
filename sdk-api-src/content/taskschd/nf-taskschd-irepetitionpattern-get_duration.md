---
UID: NF:taskschd.IRepetitionPattern.get_Duration
title: IRepetitionPattern::get_Duration method
author: windows-driver-content
description: Gets or sets how long the pattern is repeated.
old-location: taskschd\irepetitionpattern_duration.htm
old-project: TaskSchd
ms.assetid: 86deb09e-d6ad-4a8d-9fdf-e3bc5ee73b1f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Duration property [Task Scheduler], Duration property [Task Scheduler], IRepetitionPattern interface, IRepetitionPattern, IRepetitionPattern interface [Task Scheduler], Duration property, IRepetitionPattern.Duration, IRepetitionPattern::get_Duration, IRepetitionPattern::put_Duration, get_Duration,IRepetitionPattern.get_Duration, taskschd.irepetitionpattern_duration, taskschd/IRepetitionPattern::Duration, taskschd/IRepetitionPattern::get_Duration, taskschd/IRepetitionPattern::put_Duration
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
-	IRepetitionPattern.Duration
-	IRepetitionPattern.get_Duration
-	IRepetitionPattern.put_Duration
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRepetitionPattern::get_Duration method


## -description


Gets or sets how long the pattern is repeated.

This property is read/write.


## -parameters


## -remarks



If you specify a repetition duration for a task, you must also specify the repetition interval.

When reading or writing XML for a task, the repetition duration is specified in the  <a href="https://msdn.microsoft.com/a24f3827-18b2-465e-b132-77dce139e0d4">Duration</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/7eea143b-d2f8-44d2-a3ec-8328a0bc69ef">IRepetitionPattern</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

