---
UID: NF:taskschd.ITaskHandler.Start
title: ITaskHandler::Start (taskschd.h)
description: Called to start the COM handler.
old-location: taskschd\itaskhandler_start.htm
tech.root: taskschd
ms.assetid: e0a51387-e638-40ee-a4e4-edd7f3115975
ms.date: 12/05/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Start method, ITaskHandler.Start, ITaskHandler::Start, Start, Start method [Task Scheduler], Start method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_start, taskschd/ITaskHandler::Start
ms.topic: method
f1_keywords:
- taskschd/ITaskHandler.Start
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- taskschd.dll
api_name:
- ITaskHandler.Start
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskHandler::Start


## -description


Called to start the COM handler. This method must be implemented by the handler.


## -parameters




### -param pHandlerServices [in]

An <b>IUnkown</b> interface that is used to communicate back with the Task Scheduler.


### -param data [in]

The arguments that are required by the handler.  These arguments are defined in the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data">Data</a> property of the COM handler action.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When implementing this method, the handler should return control immediately to the Task Scheduler (starting its own thread if inproc).

After  the handler starts its processing, it can call the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-updatestatus">UpdateStatus</a> method to indicate  its percentage of completion or call the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-taskcompleted">TaskCompleted</a> method to indicate when the handler has completed its processing. These methods are provided by the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus">ITaskHandlerStatus</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data">Data</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus">ITaskHandlerStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-taskcompleted">TaskCompleted</a>



<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskhandlerstatus-updatestatus">UpdateStatus</a>
 

 

