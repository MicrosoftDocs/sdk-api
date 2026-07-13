---
UID: NF:pla.IDataCollectorSet.get_TaskUserTextArguments
title: IDataCollectorSet::get_TaskUserTextArguments (pla.h)
description: Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in the IDataCollectorSet::TaskArguments property. (Get)
helpviewer_keywords: ["IDataCollectorSet interface [PLA]","TaskUserTextArguments property","IDataCollectorSet.TaskUserTextArguments","IDataCollectorSet.get_TaskUserTextArguments","IDataCollectorSet::TaskUserTextArguments","IDataCollectorSet::get_TaskUserTextArguments","IDataCollectorSet::put_TaskUserTextArguments","TaskUserTextArguments property [PLA]","TaskUserTextArguments property [PLA]","IDataCollectorSet interface","get_TaskUserTextArguments","pla.idatacollectorset_taskusertextarguments","pla/IDataCollectorSet::TaskUserTextArguments","pla/IDataCollectorSet::get_TaskUserTextArguments","pla/IDataCollectorSet::put_TaskUserTextArguments"]
old-location: pla\idatacollectorset_taskusertextarguments.htm
tech.root: PLA
ms.assetid: 99fb2ed4-525b-4733-a652-b164b2c19980
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet interface [PLA],TaskUserTextArguments property, IDataCollectorSet.TaskUserTextArguments, IDataCollectorSet.get_TaskUserTextArguments, IDataCollectorSet::TaskUserTextArguments, IDataCollectorSet::get_TaskUserTextArguments, IDataCollectorSet::put_TaskUserTextArguments, TaskUserTextArguments property [PLA], TaskUserTextArguments property [PLA],IDataCollectorSet interface, get_TaskUserTextArguments, pla.idatacollectorset_taskusertextarguments, pla/IDataCollectorSet::TaskUserTextArguments, pla/IDataCollectorSet::get_TaskUserTextArguments, pla/IDataCollectorSet::put_TaskUserTextArguments
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
 - IDataCollectorSet::get_TaskUserTextArguments
 - pla/IDataCollectorSet::get_TaskUserTextArguments
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
 - IDataCollectorSet.TaskUserTextArguments
 - IDataCollectorSet.get_TaskUserTextArguments
 - IDataCollectorSet.put_TaskUserTextArguments
---

# IDataCollectorSet::get_TaskUserTextArguments


## -description

Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a> property.

This property is read/write.

## -parameters

## -remarks

These arguments are included in the command-line arguments passed to the Task Scheduler job only if the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">TaskArguments</a> property includes the  {usertext} substitution variable. 

PLA provides the following substitution variables that you can include in your arguments string. PLA provides the values for the substitution variables when the task is triggered. You do not escape the braces.

<table>
<tr>
<th>Variable</th>
<th>Description</th>
</tr>
<tr>
<td>{key}</td>
<td>Space-delimited list of key values that were specified using the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setvalue">IDataCollectorSet::SetValue</a> method.</td>
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

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorset">IDataCollectorSet</a>



<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a>
