---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

