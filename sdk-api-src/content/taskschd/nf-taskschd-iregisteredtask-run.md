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

# IRegisteredTask::Run


## -description


Runs the registered task immediately.


## -parameters




### -param params [in]

The parameters used as  values in the task actions. To not specify any parameter values for the task actions, set this parameter to <b>VT_NULL</b> or <b>VT_EMPTY</b>. Otherwise, a single <b>BSTR</b> value or an array of <b>BSTR</b> values can be specified.

The <b>BSTR</b> values that you specify are paired with names and stored as name-value pairs.  If you specify a single <b>BSTR</b> value, then Arg0 will be the name assigned to the value. The value can be used in the task action where the $(Arg0) variable is used in the action properties.

If you pass in values such as "0", "100", and "250" as an array of <b>BSTR</b> values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables that are used in the action properties.

A maximum of 32 <b>BSTR</b> values can be specified.

For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see <a href="https://msdn.microsoft.com/4cbe739d-4c4e-4469-8289-4be41b93950c">Task Actions</a>.


### -param ppRunningTask [out, optional]

An <a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a> interface that  defines the new instance of the task. 

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method will return without error, but the task will not run if the <a href="https://msdn.microsoft.com/267cf3c3-0e18-4a4f-bb32-d6766ceb6241">AllowDemandStart</a> property of ITaskSettings is set to false for the task.

The <b>IRegisteredTask::Run</b> function is equivalent to the <a href="https://msdn.microsoft.com/d6d09ab1-026d-4ee9-b520-c7702e37504e">IRegisteredTask::RunEx</a> function with the flags parameter equal to 0 and the user parameter equal to <b>NULL</b>.

If <b>IRegisteredTask::Run</b> is invoked from a disabled task, it will return SCHED_E_TASK_DISABLED.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

