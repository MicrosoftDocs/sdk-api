---
UID: NF:pla.IAlertDataCollector.put_TaskUserTextArguments
title: IAlertDataCollector::put_TaskUserTextArguments
author: windows-sdk-content
description: Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the IAlertDataCollector::Task property.
old-location: pla\ialertdatacollector_taskusertextarguments.htm
tech.root: pla
ms.assetid: d432652a-3dea-43f0-a698-bb7ccb1cb79a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAlertDataCollector interface [PLA],TaskUserTextArguments property, IAlertDataCollector.TaskUserTextArguments, IAlertDataCollector.put_TaskUserTextArguments, IAlertDataCollector::TaskUserTextArguments, IAlertDataCollector::get_TaskUserTextArguments, IAlertDataCollector::put_TaskUserTextArguments, TaskUserTextArguments property [PLA], TaskUserTextArguments property [PLA],IAlertDataCollector interface, pla.ialertdatacollector_taskusertextarguments, pla/IAlertDataCollector::TaskUserTextArguments, pla/IAlertDataCollector::get_TaskUserTextArguments, pla/IAlertDataCollector::put_TaskUserTextArguments, put_TaskUserTextArguments
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
 - IAlertDataCollector.TaskUserTextArguments
 - IAlertDataCollector.get_TaskUserTextArguments
 - IAlertDataCollector.put_TaskUserTextArguments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAlertDataCollector::put_TaskUserTextArguments


## -description


Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the <a href="https://msdn.microsoft.com/a86f8524-3564-4a65-9574-1709f82280d8">IAlertDataCollector::Task</a> property.

This property is read/write.


## -parameters


## -remarks



These arguments are included in the command-line arguments passed to the Task Scheduler job only if the <a href="https://msdn.microsoft.com/3062688f-a612-4824-beae-b75687b4feed">IAlertDataCollector::TaskArguments</a> property includes the  {usertext} substitution variable. 

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




<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
 

 

