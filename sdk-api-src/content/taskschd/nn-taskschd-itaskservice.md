---
UID: NN:taskschd.ITaskService
title: ITaskService (taskschd.h)
description: Provides access to the Task Scheduler service for managing registered tasks.
helpviewer_keywords: ["ITaskService","ITaskService interface [Task Scheduler]","ITaskService interface [Task Scheduler]","described","taskschd.itaskservice","taskschd/ITaskService"]
old-location: taskschd\itaskservice.htm
tech.root: taskschd
ms.assetid: 2459aaae-4c3a-458a-ad2c-bfff3a0322d3
ms.date: 12/05/2018
ms.keywords: ITaskService, ITaskService interface [Task Scheduler], ITaskService interface [Task Scheduler],described, taskschd.itaskservice, taskschd/ITaskService
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
 - ITaskService
 - taskschd/ITaskService
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
 - ITaskService
---

# ITaskService interface


## -description

Provides access to the Task Scheduler service for managing registered tasks.

The <a href="/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect">ITaskService::Connect</a> method should be called before calling any of the other <b>ITaskService</b> methods.

## -inheritance

The <b>ITaskService</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskService</b> also has these types of members:

## -see-also

<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
