---
UID: NF:pla.IDataCollectorSet.put_TaskArguments
title: IDataCollectorSet::put_TaskArguments
author: windows-sdk-content
description: Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the IDataCollectorSet::Task property.
old-location: pla\idatacollectorset_get_taskarguments.htm
tech.root: pla
ms.assetid: 7bd045df-379b-40fb-b309-cec531493018
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorSet interface [PLA],TaskArguments property, IDataCollectorSet.TaskArguments, IDataCollectorSet.put_TaskArguments, IDataCollectorSet::TaskArguments, IDataCollectorSet::get_TaskArguments, IDataCollectorSet::put_TaskArguments, TaskArguments property [PLA], TaskArguments property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_taskarguments, pla.idatacollectorset_get_taskarguments, pla/IDataCollectorSet::TaskArguments, pla/IDataCollectorSet::get_TaskArguments, pla/IDataCollectorSet::put_TaskArguments, put_TaskArguments
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
 - IDataCollectorSet.TaskArguments
 - IDataCollectorSet.get_TaskArguments
 - IDataCollectorSet.put_TaskArguments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

