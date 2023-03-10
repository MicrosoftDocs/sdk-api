---
UID: NF:pla.IAlertDataCollector.put_Task
title: IAlertDataCollector::put_Task (pla.h)
description: Retrieves or sets the name of a Task Scheduler job to start each time the counter value crosses the threshold. (Put)
helpviewer_keywords: ["IAlertDataCollector interface [PLA]","Task property","IAlertDataCollector.Task","IAlertDataCollector.put_Task","IAlertDataCollector::Task","IAlertDataCollector::get_Task","IAlertDataCollector::put_Task","Task property [PLA]","Task property [PLA]","IAlertDataCollector interface","base.ialertdatacollector_task","pla.ialertdatacollector_task","pla/IAlertDataCollector::Task","pla/IAlertDataCollector::get_Task","pla/IAlertDataCollector::put_Task","put_Task"]
old-location: pla\ialertdatacollector_task.htm
tech.root: PLA
ms.assetid: a86f8524-3564-4a65-9574-1709f82280d8
ms.date: 12/05/2018
ms.keywords: IAlertDataCollector interface [PLA],Task property, IAlertDataCollector.Task, IAlertDataCollector.put_Task, IAlertDataCollector::Task, IAlertDataCollector::get_Task, IAlertDataCollector::put_Task, Task property [PLA], Task property [PLA],IAlertDataCollector interface, base.ialertdatacollector_task, pla.ialertdatacollector_task, pla/IAlertDataCollector::Task, pla/IAlertDataCollector::get_Task, pla/IAlertDataCollector::put_Task, put_Task
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAlertDataCollector::put_Task
 - pla/IAlertDataCollector::put_Task
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IAlertDataCollector.Task
 - IAlertDataCollector.get_Task
 - IAlertDataCollector.put_Task
---

# IAlertDataCollector::put_Task


## -description

Retrieves or sets the name of a Task Scheduler job to start each time the counter value crosses the threshold. 

This property is read/write.

## -parameters

## -remarks

To specify command-line arguments for the task, see the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_taskarguments">IAlertDataCollector::TaskArguments</a> and <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_taskusertextarguments">IAlertDataCollector::TaskUserTextArguments</a> properties. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
