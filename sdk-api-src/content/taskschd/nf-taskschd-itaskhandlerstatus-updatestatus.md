---
UID: NF:taskschd.ITaskHandlerStatus.UpdateStatus
title: ITaskHandlerStatus::UpdateStatus (taskschd.h)
author: windows-sdk-content
description: Tells the Task Scheduler about the percentage of completion of the COM handler.
old-location: taskschd\itaskhandlerstatus_updatestatus.htm
tech.root: taskschd
ms.assetid: 3cab2b3b-7293-4d06-843f-9151d62d4950
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITaskHandlerStatus interface [Task Scheduler],UpdateStatus method, ITaskHandlerStatus.UpdateStatus, ITaskHandlerStatus::UpdateStatus, UpdateStatus, UpdateStatus method [Task Scheduler], UpdateStatus method [Task Scheduler],ITaskHandlerStatus interface, taskschd.itaskhandlerstatus_updatestatus, taskschd/ITaskHandlerStatus::UpdateStatus
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
 - ITaskHandlerStatus.UpdateStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskHandlerStatus::UpdateStatus


## -description


Tells the Task Scheduler about the percentage of completion of the COM handler.


## -parameters




### -param percentComplete [in]

A value that indicates the percentage of completion for the COM handler.


### -param statusMessage [in]

The message that is displayed in the Task Scheduler UI.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8b846be3-f05f-4d90-9865-da245c2bfdbf">ITaskHandlerStatus</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

