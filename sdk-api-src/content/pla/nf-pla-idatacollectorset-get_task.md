---
UID: NF:pla.IDataCollectorSet.get_Task
title: IDataCollectorSet::get_Task (pla.h)
description: Retrieves or sets the name of a Task Scheduler job to start each time the data collector set stops, including between segments.helpviewer_keywords: ["IDataCollectorSet interface [PLA]","Task property","IDataCollectorSet.Task","IDataCollectorSet.get_Task","IDataCollectorSet::Task","IDataCollectorSet::get_Task","IDataCollectorSet::put_Task","Task property [PLA]","Task property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_task","get_Task","pla.idatacollectorset_get_task","pla/IDataCollectorSet::Task","pla/IDataCollectorSet::get_Task","pla/IDataCollectorSet::put_Task"]
old-location: pla\idatacollectorset_get_task.htm
tech.root: PLA
ms.assetid: 8a89ebb9-2396-43f9-81ee-bfc2cdff18fa
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],Task property, IDataCollectorSet.Task, IDataCollectorSet.get_Task, IDataCollectorSet::Task, IDataCollectorSet::get_Task, IDataCollectorSet::put_Task, Task property [PLA], Task property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_task, get_Task, pla.idatacollectorset_get_task, pla/IDataCollectorSet::Task, pla/IDataCollectorSet::get_Task, pla/IDataCollectorSet::put_Task
f1_keywords:
- pla/IDataCollectorSet.Task
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorSet::get_Task


## -description


Retrieves or sets the name of a <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> job to start each time the data collector set stops, including between segments.

This property is read/write.


## -parameters


## -remarks



To specify command-line arguments for the task, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">IDataCollectorSet::TaskUserTextArguments</a>. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">IDataCollectorSet::TaskUserTextArguments</a>
 

 

