---
UID: NN:mstask.ITaskScheduler
title: ITaskScheduler (mstask.h)
description: Provides the methods for scheduling tasks.
helpviewer_keywords: ["ITaskScheduler","ITaskScheduler interface [Task Scheduler]","ITaskScheduler interface [Task Scheduler]","described","_msb_itaskscheduler","mstask/ITaskScheduler","taskschd.itaskscheduler"]
old-location: taskschd\itaskscheduler.htm
tech.root: taskschd
ms.assetid: 70c276e1-a45a-4a7d-aacc-3eb647675098
ms.date: 12/05/2018
ms.keywords: ITaskScheduler, ITaskScheduler interface [Task Scheduler], ITaskScheduler interface [Task Scheduler],described, _msb_itaskscheduler, mstask/ITaskScheduler, taskschd.itaskscheduler
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
 - ITaskScheduler
 - mstask/ITaskScheduler
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
 - ITaskScheduler
---

# ITaskScheduler interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for scheduling tasks.

It is the primary interface of the <a href="/windows/desktop/TaskSchd/t">task scheduler object</a>. To create a task scheduler object, call <b>CoCreateInstance</b>.

## -inheritance

The <b>ITaskScheduler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskScheduler</b> also has these types of members:

