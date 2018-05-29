---
UID: NF:taskschd.ITaskHandler.Resume
title: ITaskHandler::Resume
author: windows-sdk-content
description: Called to resume the COM handler.
old-location: taskschd\itaskhandler_resume.htm
old-project: TaskSchd
ms.assetid: 69e82100-2f21-49a1-8ede-e106cb8f1a25
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Resume method, ITaskHandler.Resume, ITaskHandler::Resume, Resume, Resume method [Task Scheduler], Resume method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_resume, taskschd/ITaskHandler::Resume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	ITaskHandler.Resume
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskHandler::Resume


## -description


Called to resume the COM handler. This method is optional and should only be implemented to give the Task Scheduler the ability to resume the handler.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

