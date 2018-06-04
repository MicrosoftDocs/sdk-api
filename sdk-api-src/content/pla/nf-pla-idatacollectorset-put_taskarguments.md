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

# IDataCollectorSet::put_TaskArguments


## -description


Retrieves or sets the command-line arguments to pass to the <a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a> job specified in the <a href="https://msdn.microsoft.com/8a89ebb9-2396-43f9-81ee-bfc2cdff18fa">IDataCollectorSet::Task</a> property.

This property is read/write.


## -parameters


## -remarks



PLA provides the following substitution variables that you can include in your arguments string. PLA provides the values for the substitution variables when the task is triggered. You must escape the braces, for example, \{name\}.

<table>
<tr>
<th>Variable</th>
<th>Description</th>
</tr>
<tr>
<td>{key}</td>
<td>Space-delimited list of key values that were specified using the  <a href="https://msdn.microsoft.com/d2143de9-f189-47e0-8b28-0422d9984459">IDataCollectorSet::SetValue</a> method.</td>
</tr>
<tr>
<td>{logs}</td>
<td>Space-delimited list of full paths to the current data collector files.</td>
</tr>
<tr>
<td>{state}</td>
<td>Indicates whether the set is running (1 for running, 0 for stopped).</td>
</tr>
<tr>
<td>{usertext}</td>
<td>String from the <a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a> property.</td>
</tr>
</table>
 

Typically, if you use the substitution variables, you specify them in <a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">TaskUserTextArguments</a>, where you do not have to escape the braces and then specify {usertext} in this property.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/8a89ebb9-2396-43f9-81ee-bfc2cdff18fa">IDataCollectorSet::Task</a>



<a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">IDataCollectorSet::TaskUserTextArguments</a>
 

 

