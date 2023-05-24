---
UID: NF:pla.IAlertDataCollector.put_TaskUserTextArguments
title: IAlertDataCollector::put_TaskUserTextArguments (pla.h)
description: Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the IAlertDataCollector::Task property. (IAlertDataCollector.put_TaskUserTextArguments)
helpviewer_keywords: ["IAlertDataCollector interface [PLA]","TaskUserTextArguments property","IAlertDataCollector.TaskUserTextArguments","IAlertDataCollector.put_TaskUserTextArguments","IAlertDataCollector::TaskUserTextArguments","IAlertDataCollector::get_TaskUserTextArguments","IAlertDataCollector::put_TaskUserTextArguments","TaskUserTextArguments property [PLA]","TaskUserTextArguments property [PLA]","IAlertDataCollector interface","pla.ialertdatacollector_taskusertextarguments","pla/IAlertDataCollector::TaskUserTextArguments","pla/IAlertDataCollector::get_TaskUserTextArguments","pla/IAlertDataCollector::put_TaskUserTextArguments","put_TaskUserTextArguments"]
old-location: pla\ialertdatacollector_taskusertextarguments.htm
tech.root: PLA
ms.assetid: d432652a-3dea-43f0-a698-bb7ccb1cb79a
ms.date: 12/05/2018
ms.keywords: IAlertDataCollector interface [PLA],TaskUserTextArguments property, IAlertDataCollector.TaskUserTextArguments, IAlertDataCollector.put_TaskUserTextArguments, IAlertDataCollector::TaskUserTextArguments, IAlertDataCollector::get_TaskUserTextArguments, IAlertDataCollector::put_TaskUserTextArguments, TaskUserTextArguments property [PLA], TaskUserTextArguments property [PLA],IAlertDataCollector interface, pla.ialertdatacollector_taskusertextarguments, pla/IAlertDataCollector::TaskUserTextArguments, pla/IAlertDataCollector::get_TaskUserTextArguments, pla/IAlertDataCollector::put_TaskUserTextArguments, put_TaskUserTextArguments
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
 - IAlertDataCollector::put_TaskUserTextArguments
 - pla/IAlertDataCollector::put_TaskUserTextArguments
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
 - IAlertDataCollector.TaskUserTextArguments
 - IAlertDataCollector.get_TaskUserTextArguments
 - IAlertDataCollector.put_TaskUserTextArguments
---

# IAlertDataCollector::put_TaskUserTextArguments


## -description

Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_task">IAlertDataCollector::Task</a> property.

This property is read/write.

## -parameters

## -remarks

These arguments are included in the command-line arguments passed to the Task Scheduler job only if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_taskarguments">IAlertDataCollector::TaskArguments</a> property includes the  {usertext} substitution variable. 

PLA provides the following substitution variables that you can include in your arguments string. PLA provides the values for the substitution variables when the alert is triggered. You do not escape the braces.

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
<td>{value}</td>
<td>Value of the performance counter.</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
