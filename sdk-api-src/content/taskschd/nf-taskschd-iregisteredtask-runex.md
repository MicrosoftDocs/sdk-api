---
UID: NF:taskschd.IRegisteredTask.RunEx
title: IRegisteredTask::RunEx
author: windows-sdk-content
description: Runs the registered task immediately using specified flags and a session identifier.
old-location: taskschd\iregisteredtask_runex.htm
tech.root: taskschd
ms.assetid: d6d09ab1-026d-4ee9-b520-c7702e37504e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRegisteredTask interface [Task Scheduler],RunEx method, IRegisteredTask.RunEx, IRegisteredTask::RunEx, RunEx, RunEx method [Task Scheduler], RunEx method [Task Scheduler],IRegisteredTask interface, taskschd.iregisteredtask_runex, taskschd/IRegisteredTask::RunEx
ms.topic: method
req.header: taskschd.h
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRegisteredTask.RunEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRegisteredTask::RunEx


## -description


Runs the registered task immediately using specified flags and a session identifier.


## -parameters




### -param params [in]

The parameters used as  values in the task actions. To not specify any parameter values for the task actions, set this parameter to <b>VT_NULL</b> or <b>VT_EMPTY</b>. Otherwise, a single <b>BSTR</b> value, or an array of <b>BSTR</b> values, can be specified.

The <b>BSTR</b> values that you specify are paired with names and stored as name-value pairs.  If you specify a single BSTR value, then Arg0 will be the name assigned to the value. The value can be used in the task action where the $(Arg0) variable is used in the action properties.

If you pass in values such as "0", "100", and "250" as an array of <b>BSTR</b> values, then "0" will replace the $(Arg0) variables, "100" will replace the $(Arg1) variables, and "250" will replace the $(Arg2) variables that are used in the action properties.

A maximum of 32 <b>BSTR</b> values can be specified.

For more information and a list of action properties that can use $(Arg0), $(Arg1), ..., $(Arg32) variables in their values, see <a href="https://msdn.microsoft.com/4cbe739d-4c4e-4469-8289-4be41b93950c">Task Actions</a>.


### -param flags [in]

A <a href="https://msdn.microsoft.com/6c5a4ab6-b3ca-4d60-918d-82797782d66a">TASK_RUN_FLAGS</a> constant that defines how the task is run.


### -param sessionID [in]

The terminal server session in which you want to start the task.

If the TASK_RUN_USE_SESSION_ID constant is not passed into the <i>flags</i> parameter, then the value specified in this parameter is ignored. If the TASK_RUN_USE_SESSION_ID constant is passed into the <i>flags</i> parameter and the sessionID value is less than or equal to 0, then an invalid argument error will be returned.

If the <b>TASK_RUN_USE_SESSION_ID</b> constant is passed into the <i>flags</i> parameter and the sessionID value is a valid session ID greater than 0 and if no value is specified for the <i>user</i> parameter, then the Task Scheduler service will try to start the task interactively as the user who is logged on to the specified session.

If the <b>TASK_RUN_USE_SESSION_ID</b> constant is passed into the <i>flags</i> parameter and the sessionID value is a valid session ID greater than 0 and if a user is specified in the <i>user</i> parameter, then the Task Scheduler service will try to start the task interactively as the user who is specified in the <i>user</i> parameter.


### -param user [in]

The user for which  the task runs.


### -param ppRunningTask [out, optional]

An <a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a> interface that  defines the new instance of the task.

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a> interface pointer.  Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method will return without error, but the task will not run if the <a href="https://msdn.microsoft.com/267cf3c3-0e18-4a4f-bb32-d6766ceb6241">AllowDemandStart</a> property of ITaskSettings is set to false for the task.

If <b>IRegisteredTask::RunEx</b> is invoked from a disabled task, it will return S_OK, but the task will not be run.




## -see-also




<a href="https://msdn.microsoft.com/3743d012-ad7c-402f-8859-939bb01ee447">IRegisteredTask</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

