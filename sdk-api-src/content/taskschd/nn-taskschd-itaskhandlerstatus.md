---
UID: NN:taskschd.ITaskHandlerStatus
title: ITaskHandlerStatus (taskschd.h)
description: Provides the methods that are used by COM handlers to notify the Task Scheduler about the status of the handler.
helpviewer_keywords: ["ITaskHandlerStatus","ITaskHandlerStatus interface [Task Scheduler]","ITaskHandlerStatus interface [Task Scheduler]","described","taskschd.itaskhandlerstatus","taskschd/ITaskHandlerStatus"]
old-location: taskschd\itaskhandlerstatus.htm
tech.root: taskschd
ms.assetid: 8b846be3-f05f-4d90-9865-da245c2bfdbf
ms.date: 12/05/2018
ms.keywords: ITaskHandlerStatus, ITaskHandlerStatus interface [Task Scheduler], ITaskHandlerStatus interface [Task Scheduler],described, taskschd.itaskhandlerstatus, taskschd/ITaskHandlerStatus
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
 - ITaskHandlerStatus
 - taskschd/ITaskHandlerStatus
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
 - ITaskHandlerStatus
---

# ITaskHandlerStatus interface


## -description

Provides the methods that are used by COM handlers to notify the Task Scheduler about the status of the handler.

## -inheritance

The <b>ITaskHandlerStatus</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskHandlerStatus</b> also has these types of members:

## -remarks

For information on specifying a COM handler action, see the <a href="/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction">IComHandlerAction</a> interface.

For information on the required interfaces that must be implemented by the handler, see the  <a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a> interface.

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
