---
UID: NF:pla.IDataCollectorSet.get_TaskArguments
title: IDataCollectorSet::get_TaskArguments (pla.h)
description: Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the IDataCollectorSet::Task property. (Get)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","TaskArguments property","IDataCollectorSet.TaskArguments","IDataCollectorSet.get_TaskArguments","IDataCollectorSet::TaskArguments","IDataCollectorSet::get_TaskArguments","IDataCollectorSet::put_TaskArguments","TaskArguments property [PLA]","TaskArguments property [PLA]","IDataCollectorSet interface","base.idatacollectorset_get_taskarguments","get_TaskArguments","pla.idatacollectorset_get_taskarguments","pla/IDataCollectorSet::TaskArguments","pla/IDataCollectorSet::get_TaskArguments","pla/IDataCollectorSet::put_TaskArguments"]
old-location: pla\idatacollectorset_get_taskarguments.htm
tech.root: PLA
ms.assetid: 7bd045df-379b-40fb-b309-cec531493018
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],TaskArguments property, IDataCollectorSet.TaskArguments, IDataCollectorSet.get_TaskArguments, IDataCollectorSet::TaskArguments, IDataCollectorSet::get_TaskArguments, IDataCollectorSet::put_TaskArguments, TaskArguments property [PLA], TaskArguments property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_taskarguments, get_TaskArguments, pla.idatacollectorset_get_taskarguments, pla/IDataCollectorSet::TaskArguments, pla/IDataCollectorSet::get_TaskArguments, pla/IDataCollectorSet::put_TaskArguments
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
 - IDataCollectorSet::get_TaskArguments
 - pla/IDataCollectorSet::get_TaskArguments
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
 - IDataCollectorSet.TaskArguments
 - IDataCollectorSet.get_TaskArguments
 - IDataCollectorSet.put_TaskArguments
---

# IDataCollectorSet::get_TaskArguments


## -description

Retrieves or sets the command-line arguments to pass to the <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> job specified in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_task">IDataCollectorSet::Task</a> property.

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
<td>Space-delimited list of key values that were specified using the  <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setvalue">IDataCollectorSet::SetValue</a> method.</td>
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
<td>String from the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">IDataCollectorSet::TaskUserTextArguments</a> property.</td>
</tr>
</table>
 

Typically, if you use the substitution variables, you specify them in <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">TaskUserTextArguments</a>, where you do not have to escape the braces and then specify {usertext} in this property.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_task">IDataCollectorSet::Task</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">IDataCollectorSet::TaskUserTextArguments</a>
