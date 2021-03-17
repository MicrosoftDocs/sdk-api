---
UID: NN:taskschd.IComHandlerAction
title: IComHandlerAction (taskschd.h)
description: Represents an action that fires a handler.
helpviewer_keywords: ["COM handler action [Task Scheduler]","interface","IComHandlerAction","IComHandlerAction interface [Task Scheduler]","IComHandlerAction interface [Task Scheduler]","described","taskschd.icomhandleraction","taskschd/IComHandlerAction"]
old-location: taskschd\icomhandleraction.htm
tech.root: taskschd
ms.assetid: fb5cc2c3-ba86-401a-b51f-b28d1f5be58f
ms.date: 12/05/2018
ms.keywords: COM handler action [Task Scheduler],interface, IComHandlerAction, IComHandlerAction interface [Task Scheduler], IComHandlerAction interface [Task Scheduler],described, taskschd.icomhandleraction, taskschd/IComHandlerAction
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
 - IComHandlerAction
 - taskschd/IComHandlerAction
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
 - IComHandlerAction
---

# IComHandlerAction interface


## -description

Represents an action that fires a handler.

## -remarks

COM handlers must implement the <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a> interface for the Task Scheduler to start and stop the handler. In turn, the COM handler uses the methods of the <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus">ITaskHandlerStatus</a> interface to communicate the status back to the Task Scheduler.

When reading or writing XML, a COM handler action is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-comhandler-actiongroup-element">ComHandler</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus">ITaskHandlerStatus</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>