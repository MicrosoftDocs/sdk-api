---
UID: NN:mstask.ITaskTrigger
title: ITaskTrigger (mstask.h)
description: Provides the methods for accessing and setting triggers for a task. Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.
helpviewer_keywords: ["ITaskTrigger","ITaskTrigger interface [Task Scheduler]","ITaskTrigger interface [Task Scheduler]","described","_msb_itasktrigger","mstask/ITaskTrigger","taskschd.itasktrigger","triggers [Task Scheduler]","interfaces","ITaskTrigger (obsolete)"]
old-location: taskschd\itasktrigger.htm
tech.root: taskschd
ms.assetid: 990702f4-fb6f-47a7-b538-f6632f831a4e
ms.date: 12/05/2018
ms.keywords: ITaskTrigger, ITaskTrigger interface [Task Scheduler], ITaskTrigger interface [Task Scheduler],described, _msb_itasktrigger, mstask/ITaskTrigger, taskschd.itasktrigger, triggers [Task Scheduler],interfaces,ITaskTrigger (obsolete)
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
 - ITaskTrigger
 - mstask/ITaskTrigger
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
 - ITaskTrigger
---

# ITaskTrigger interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for accessing and setting triggers for a task. Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.

<b>ITaskTrigger</b> is the primary interface of the <a href="/windows/desktop/TaskSchd/t">task_trigger object</a>. To create a trigger object, call 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-createtrigger">CreateTrigger</a> or 
<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettrigger">GetTrigger</a>.

## -inheritance

The <b>ITaskTrigger</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskTrigger</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-createtrigger">IScheduledWorkItem::CreateTrigger</a>



<a href="/windows/desktop/api/mstask/nf-mstask-ischeduledworkitem-gettrigger">IScheduledWorkItem::GetTrigger</a>
