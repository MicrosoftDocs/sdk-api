---
UID: NN:taskschd.IComHandlerAction
title: IComHandlerAction
author: windows-sdk-content
description: Represents an action that fires a handler.
old-location: taskschd\icomhandleraction.htm
old-project: TaskSchd
ms.assetid: fb5cc2c3-ba86-401a-b51f-b28d1f5be58f
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: COM handler action [Task Scheduler],interface, IComHandlerAction, IComHandlerAction interface [Task Scheduler], IComHandlerAction interface [Task Scheduler],described, taskschd.icomhandleraction, taskschd/IComHandlerAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IComHandlerAction
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComHandlerAction interface


## -description


Represents an action that fires a handler.


## -remarks



COM handlers must implement the <a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a> interface for the Task Scheduler to start and stop the handler. In turn, the COM handler uses the methods of the <a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a> interface to communicate the status back to the Task Scheduler.

When reading or writing XML, a COM handler action is specified in the <a href="https://msdn.microsoft.com/18f16873-3879-4a3b-b8f2-17cc84647e25">ComHandler</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538787">IAction</a>



<a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

