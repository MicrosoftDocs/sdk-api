---
UID: NN:mstask.IScheduledWorkItem
title: IScheduledWorkItem (mstask.h)
description: Provides the methods for managing specific work items.
helpviewer_keywords: ["IScheduledWorkItem","IScheduledWorkItem interface [Task Scheduler]","IScheduledWorkItem interface [Task Scheduler]","described","_msb_ischeduledworkitem","mstask/IScheduledWorkItem","taskschd.ischeduledworkitem"]
old-location: taskschd\ischeduledworkitem.htm
tech.root: taskschd
ms.assetid: e668833a-094d-4504-90a0-87912a6a53c2
ms.date: 12/05/2018
ms.keywords: IScheduledWorkItem, IScheduledWorkItem interface [Task Scheduler], IScheduledWorkItem interface [Task Scheduler],described, _msb_ischeduledworkitem, mstask/IScheduledWorkItem, taskschd.ischeduledworkitem
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
 - IScheduledWorkItem
 - mstask/IScheduledWorkItem
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
 - IScheduledWorkItem
---

# IScheduledWorkItem interface


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods for managing specific <a href="/windows/desktop/TaskSchd/w">work items</a>.

## -inheritance

The <b>IScheduledWorkItem</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IScheduledWorkItem</b> also has these types of members:

## -remarks

The <b>IScheduledWorkItem</b> interface is the base interface for the 
<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a> interface. All methods provided by 
<b>IScheduledWorkItem</b> are inherited by the 
<b>ITask</b> interface and are typically called through that interface.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/c-c-code-example-terminating-a-task">C/C++ Code Example: Terminating a Task</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itask">ITask</a>
