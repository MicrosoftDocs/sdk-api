---
UID: NF:taskschd.ITaskHandler.Stop
title: ITaskHandler::Stop (taskschd.h)
description: Called to stop the COM handler.
helpviewer_keywords: ["ITaskHandler interface [Task Scheduler]","Stop method","ITaskHandler.Stop","ITaskHandler::Stop","Stop","Stop method [Task Scheduler]","Stop method [Task Scheduler]","ITaskHandler interface","taskschd.itaskhandler_stop","taskschd/ITaskHandler::Stop"]
old-location: taskschd\itaskhandler_stop.htm
tech.root: taskschd
ms.assetid: 93a112e7-5e44-42a9-a5f5-d61e1ad1eabc
ms.date: 12/05/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Stop method, ITaskHandler.Stop, ITaskHandler::Stop, Stop, Stop method [Task Scheduler], Stop method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_stop, taskschd/ITaskHandler::Stop
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
 - ITaskHandler::Stop
 - taskschd/ITaskHandler::Stop
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
 - ITaskHandler.Stop
---

# ITaskHandler::Stop


## -description

Called to stop the COM handler. This method must be implemented by the handler.

## -parameters

### -param pRetCode [out]

The return code that the Task Schedule will raise as an event when the COM handler action is completed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>