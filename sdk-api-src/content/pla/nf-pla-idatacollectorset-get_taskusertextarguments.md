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

# IDataCollectorSet::get_TaskUserTextArguments


## -description


Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in the <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> property.

This property is read/write.


## -parameters


## -remarks



These arguments are included in the command-line arguments passed to the Task Scheduler job only if the <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">TaskArguments</a> property includes the  {usertext} substitution variable. 

PLA provides the following substitution variables that you can include in your arguments string. PLA provides the values for the substitution variables when the task is triggered. You do not escape the braces.

<table>
<tr>
<th>Variable</th>
<th>Description</th>
</tr>
<tr>
<td>{key}</td>
<td>Space-delimited list of key values that were specified using the <a href="https://msdn.microsoft.com/d2143de9-f189-47e0-8b28-0422d9984459">IDataCollectorSet::SetValue</a> method.</td>
</tr>
<tr>
<td>{logs}</td>
<td>Space-delimited list of full paths to the current data collector files.</td>
</tr>
<tr>
<td>{state}</td>
<td> Indicates whether the set is running (1 for running, 0 for stopped).</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a>
 

 

