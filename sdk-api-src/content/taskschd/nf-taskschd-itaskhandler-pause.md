---
UID: NF:taskschd.ITaskHandler.Pause
title: ITaskHandler::Pause method
author: windows-driver-content
description: Called to pause the COM handler.
old-location: taskschd\itaskhandler_pause.htm
old-project: TaskSchd
ms.assetid: 851e3f20-a996-4a4b-bf10-7ba5c79c3d82
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ITaskHandler, ITaskHandler interface [Task Scheduler], Pause method, ITaskHandler::Pause, Pause method [Task Scheduler], Pause method [Task Scheduler], ITaskHandler interface, Pause,ITaskHandler.Pause, taskschd.itaskhandler_pause, taskschd/ITaskHandler::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ITaskHandler.Pause
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskHandler::Pause method


## -description


Called to pause the COM handler. This method is optional and should only be implemented to give the Task Scheduler the ability to pause and restart the handler.


## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

