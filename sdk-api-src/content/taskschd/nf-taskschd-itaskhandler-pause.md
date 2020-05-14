---
UID: NF:taskschd.ITaskHandler.Pause
title: ITaskHandler::Pause (taskschd.h)
description: Called to pause the COM handler.helpviewer_keywords: ["ITaskHandler interface [Task Scheduler]","Pause method","ITaskHandler.Pause","ITaskHandler::Pause","Pause","Pause method [Task Scheduler]","Pause method [Task Scheduler]","ITaskHandler interface","taskschd.itaskhandler_pause","taskschd/ITaskHandler::Pause"]
old-location: taskschd\itaskhandler_pause.htm
tech.root: taskschd
ms.assetid: 851e3f20-a996-4a4b-bf10-7ba5c79c3d82
ms.date: 12/05/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Pause method, ITaskHandler.Pause, ITaskHandler::Pause, Pause, Pause method [Task Scheduler], Pause method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_pause, taskschd/ITaskHandler::Pause
f1_keywords:
- taskschd/ITaskHandler.Pause
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
- ITaskHandler.Pause
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskHandler::Pause


## -description


Called to pause the COM handler. This method is optional and should only be implemented to give the Task Scheduler the ability to pause and restart the handler.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
 

 

