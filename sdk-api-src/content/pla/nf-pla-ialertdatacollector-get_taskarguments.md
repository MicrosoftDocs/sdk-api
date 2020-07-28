---
UID: NF:pla.IAlertDataCollector.get_TaskArguments
title: IAlertDataCollector::get_TaskArguments (pla.h)
description: Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the IAlertDataCollector::Task property.
helpviewer_keywords: ["IAlertDataCollector interface [PLA]","TaskArguments property","IAlertDataCollector.TaskArguments","IAlertDataCollector.get_TaskArguments","IAlertDataCollector::TaskArguments","IAlertDataCollector::get_TaskArguments","IAlertDataCollector::put_TaskArguments","TaskArguments property [PLA]","TaskArguments property [PLA]","IAlertDataCollector interface","base.ialertdatacollector_taskarguments","get_TaskArguments","pla.ialertdatacollector_taskarguments","pla/IAlertDataCollector::TaskArguments","pla/IAlertDataCollector::get_TaskArguments","pla/IAlertDataCollector::put_TaskArguments"]
old-location: pla\ialertdatacollector_taskarguments.htm
tech.root: PLA
ms.assetid: 3062688f-a612-4824-beae-b75687b4feed
ms.date: 12/05/2018
ms.keywords: IAlertDataCollector interface [PLA],TaskArguments property, IAlertDataCollector.TaskArguments, IAlertDataCollector.get_TaskArguments, IAlertDataCollector::TaskArguments, IAlertDataCollector::get_TaskArguments, IAlertDataCollector::put_TaskArguments, TaskArguments property [PLA], TaskArguments property [PLA],IAlertDataCollector interface, base.ialertdatacollector_taskarguments, get_TaskArguments, pla.ialertdatacollector_taskarguments, pla/IAlertDataCollector::TaskArguments, pla/IAlertDataCollector::get_TaskArguments, pla/IAlertDataCollector::put_TaskArguments
f1_keywords:
- pla/IAlertDataCollector.TaskArguments
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
- IAlertDataCollector.TaskArguments
- IAlertDataCollector.get_TaskArguments
- IAlertDataCollector.put_TaskArguments
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAlertDataCollector::get_TaskArguments


## -description


Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_task">IAlertDataCollector::Task</a> property.

This property is read/write.


## -parameters


## -remarks



If the task to run is a script, you must set the task arguments in the Task Scheduler to $(Arg0); otherwise, the arguments that you specify with this property will not be passed to the script.

PLA provides the following substitution variables that you can include in your arguments string. PLA provides the values for the substitution variables when the alert is triggered. You must escape the braces, for example, \{name\}.

<table>
<tr>
<th>Variable</th>
<th>Description</th>
</tr>
<tr>
<td>{counter}</td>
<td> Path of the performance counter that crossed the threshold.</td>
</tr>
<tr>
<td>{date}</td>
<td>Time that the threshold was crossed.</td>
</tr>
<tr>
<td>{name}</td>
<td>Name of the alert data collector.</td>
</tr>
<tr>
<td>{threshold}</td>
<td>Value of the threshold.</td>
</tr>
<tr>
<td>{usertext}</td>
<td>String from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_taskusertextarguments">IAlertDataCollector::TaskUserTextArguments</a> property.</td>
</tr>
<tr>
<td>{value}</td>
<td>Value of the performance counter.</td>
</tr>
</table>
 

Typically, if you use the substitution variables, you specify them in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_taskusertextarguments">TaskUserTextArguments</a>, where you do not have to escape the braces, and then specify {usertext} in this property.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
 

 

