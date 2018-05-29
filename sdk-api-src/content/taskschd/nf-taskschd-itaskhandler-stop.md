---
UID: NF:taskschd.ITaskHandler.Stop
title: ITaskHandler::Stop
author: windows-sdk-content
description: Called to stop the COM handler.
old-location: taskschd\itaskhandler_stop.htm
old-project: TaskSchd
ms.assetid: 93a112e7-5e44-42a9-a5f5-d61e1ad1eabc
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskHandler interface [Task Scheduler],Stop method, ITaskHandler.Stop, ITaskHandler::Stop, Stop, Stop method [Task Scheduler], Stop method [Task Scheduler],ITaskHandler interface, taskschd.itaskhandler_stop, taskschd/ITaskHandler::Stop
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
-	ITaskHandler.Stop
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskHandler::Stop


## -description


Called to stop the COM handler. This method must be implemented by the handler.


## -parameters




### -param pRetCode [out]

The return code that the Task Schedule will raise as an event when the COM handler action is completed.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

