---
UID: NF:pla.IAlertDataCollector.put_Task
title: IAlertDataCollector::put_Task
author: windows-driver-content
description: Retrieves or sets the name of a Task Scheduler job to start each time the counter value crosses the threshold.
old-location: pla\ialertdatacollector_task.htm
old-project: PLA
ms.assetid: a86f8524-3564-4a65-9574-1709f82280d8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IAlertDataCollector interface [PLA],Task property, IAlertDataCollector.Task, IAlertDataCollector.put_Task, IAlertDataCollector::Task, IAlertDataCollector::get_Task, IAlertDataCollector::put_Task, Task property [PLA], Task property [PLA],IAlertDataCollector interface, base.ialertdatacollector_task, pla.ialertdatacollector_task, pla/IAlertDataCollector::Task, pla/IAlertDataCollector::get_Task, pla/IAlertDataCollector::put_Task, put_Task
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IAlertDataCollector.Task
-	IAlertDataCollector.get_Task
-	IAlertDataCollector.put_Task
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAlertDataCollector::put_Task


## -description


Retrieves or sets the name of a Task Scheduler job to start each time the counter value crosses the threshold. 

This property is read/write.


## -parameters


## -remarks



To specify command-line arguments for the task, see the <a href="https://msdn.microsoft.com/3062688f-a612-4824-beae-b75687b4feed">IAlertDataCollector::TaskArguments</a> and <a href="https://msdn.microsoft.com/d432652a-3dea-43f0-a698-bb7ccb1cb79a">IAlertDataCollector::TaskUserTextArguments</a> properties. 

To start the task in the directory where PLA is collecting the data, set the task's <b>Start in</b> field to $(Arg1).




## -see-also




<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
 

 

