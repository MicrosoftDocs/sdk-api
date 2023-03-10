---
UID: NN:mstask.IProvideTaskPage
title: IProvideTaskPage (mstask.h)
description: Provides the methods to access the property sheet settings of a task.
helpviewer_keywords: ["IProvideTaskPage","IProvideTaskPage interface [Task Scheduler]","IProvideTaskPage interface [Task Scheduler]","described","_msb_iprovidetaskpage","mstask/IProvideTaskPage","taskschd.iprovidetaskpage"]
old-location: taskschd\iprovidetaskpage.htm
tech.root: taskschd
ms.assetid: 58be7ea9-022f-46a0-9f27-9b226000a8cc
ms.date: 12/05/2018
ms.keywords: IProvideTaskPage, IProvideTaskPage interface [Task Scheduler], IProvideTaskPage interface [Task Scheduler],described, _msb_iprovidetaskpage, mstask/IProvideTaskPage, taskschd.iprovidetaskpage
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
 - IProvideTaskPage
 - mstask/IProvideTaskPage
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
 - IProvideTaskPage
---

# IProvideTaskPage interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods to access the property sheet settings of a task.

## -inheritance

The <b>IProvideTaskPage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProvideTaskPage</b> also has these types of members:

## -remarks

This is the primary interface of the <a href="/windows/desktop/TaskSchd/t">task object</a>. To create a task object, call 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a> for existing tasks or 
<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">ITaskScheduler::NewWorkItem</a> for new tasks.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/c-c-code-example-retrieving-a-task-page">C/C++ Code Example: Retrieving a Task Page</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-activate">ITaskScheduler::Activate</a>



<a href="/windows/desktop/api/mstask/nf-mstask-itaskscheduler-newworkitem">ITaskScheduler::NewWorkItem</a>
