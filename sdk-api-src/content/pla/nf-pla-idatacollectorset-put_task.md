---
UID: NF:pla.IDataCollectorSet.put_Task
title: IDataCollectorSet::put_Task
author: windows-sdk-content
description: Retrieves or sets the name of a Task Scheduler job to start each time the data collector set stops, including between segments.
old-location: pla\idatacollectorset_get_task.htm
tech.root: PLA
ms.assetid: 8a89ebb9-2396-43f9-81ee-bfc2cdff18fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorSet interface [PLA],Task property, IDataCollectorSet.Task, IDataCollectorSet.put_Task, IDataCollectorSet::Task, IDataCollectorSet::get_Task, IDataCollectorSet::put_Task, Task property [PLA], Task property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_task, pla.idatacollectorset_get_task, pla/IDataCollectorSet::Task, pla/IDataCollectorSet::get_Task, pla/IDataCollectorSet::put_Task, put_Task
ms.topic: method
req.header: pla.h
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
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Task
 - IDataCollectorSet.get_Task
 - IDataCollectorSet.put_Task
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::put_Task


## -description


Retrieves or sets the name of a <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> job to start each time the data collector set stops, including between segments.

This property is read/write.


## -parameters


## -remarks



To specify command-line arguments for the task, see <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> and <a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a>. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a>



<a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a>
 

 

