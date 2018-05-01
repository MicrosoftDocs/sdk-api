---
UID: NF:pla.IDataCollectorSet.get_TaskUserTextArguments
title: IDataCollectorSet::get_TaskUserTextArguments method
author: windows-driver-content
description: Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in the IDataCollectorSet::TaskArguments property.
old-location: pla\idatacollectorset_taskusertextarguments.htm
old-project: PLA
ms.assetid: 99fb2ed4-525b-4733-a652-b164b2c19980
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataCollectorSet, IDataCollectorSet interface [PLA], TaskUserTextArguments property, IDataCollectorSet.TaskUserTextArguments, IDataCollectorSet::get_TaskUserTextArguments, IDataCollectorSet::put_TaskUserTextArguments, TaskUserTextArguments property [PLA], TaskUserTextArguments property [PLA], IDataCollectorSet interface, get_TaskUserTextArguments,IDataCollectorSet.get_TaskUserTextArguments, pla.idatacollectorset_taskusertextarguments, pla/IDataCollectorSet::TaskUserTextArguments, pla/IDataCollectorSet::get_TaskUserTextArguments, pla/IDataCollectorSet::put_TaskUserTextArguments
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
-	IDataCollectorSet.TaskUserTextArguments
-	IDataCollectorSet.get_TaskUserTextArguments
-	IDataCollectorSet.put_TaskUserTextArguments
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataCollectorSet::get_TaskUserTextArguments method


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
 

 

