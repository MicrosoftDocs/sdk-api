---
UID: NF:taskschd.ITaskHandler.Resume
title: ITaskHandler::Resume (taskschd.h)
description: Called to resume the COM handler.
helpviewer_keywords: ["ITaskHandler interface [Task Scheduler]","Resume method","ITaskHandler.Resume","ITaskHandler::Resume","Resume","Resume method [Task Scheduler]","Resume method [Task Scheduler]","ITaskHandler interface","taskschd.itaskhandler_resume","taskschd/ITaskHandler::Resume"]
old-location: taskschd\itaskhandler_resume.htm
tech.root: taskschd
ms.assetid: 69e82100-2f21-49a1-8ede-e106cb8f1a25
ms.date: 12/05/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Resume method, ITaskHandler.Resume, ITaskHandler::Resume, Resume, Resume method [Task Scheduler], Resume method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_resume, taskschd/ITaskHandler::Resume
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
 - ITaskHandler::Resume
 - taskschd/ITaskHandler::Resume
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
 - ITaskHandler.Resume
---

# ITaskHandler::Resume


## -description

Called to resume the COM handler. This method is optional and should only be implemented to give the Task Scheduler the ability to resume the handler.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskhandler">ITaskHandler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
