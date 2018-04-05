---
UID: NN:mstask.ITask
title: ITask
author: windows-driver-content
description: Defines a task.
old-location: ccp\itask.htm
old-project: CcpSdk
ms.assetid: 3118a416-14d8-4d38-a8c8-e5e7e985aeef
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: ITask, ITask interface [CCP], ITask interface [CCP], described, ccp.itask, mstask/ITask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mstask.h
req.include-header: 
req.target-type: Windows
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
req.type-library: Ccpapi.tlb
req.typenames: TASK_TRIGGER_TYPE, *PTASK_TRIGGER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ccpapi.tlb
api_name:
-	ITask
product: Windows
targetos: Windows
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITask interface


## -description


Defines a task.

To create a task, call the <a href="https://msdn.microsoft.com/6d5fd51e-cdc3-4f77-84f5-303b9d501596">ICluster::CreateTask</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITask</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee25dd75-dc28-4be4-b4cc-3a61ba1963ef">get_CommandLine</a>
</td>
<td align="left" width="63%">
Retrieves the command line for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d256f0d-5f5f-42b4-9806-6c94317be8dd">get_CreateTime</a>
</td>
<td align="left" width="63%">
Retrieves the task creation time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/796d3e48-3eb1-47ad-ba76-9fe394c4eba5">get_Depend</a>
</td>
<td align="left" width="63%">
Retrieves the dependent tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1310b505-5b51-4578-adf3-2ad037b3a140">get_EndTime</a>
</td>
<td align="left" width="63%">
Retrieves the task end time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7ab0722-9a88-433a-8f4c-464ac841f4d5">get_EnvironmentVariables</a>
</td>
<td align="left" width="63%">
Retrieves the environment variables for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c22844f-358a-477f-9088-698eee01e7d9">get_ErrorMessage</a>
</td>
<td align="left" width="63%">
Retrieves the task error message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b91e865-25e6-4139-a1cf-b1d34d26783f">get_ExitCode</a>
</td>
<td align="left" width="63%">
Retrieves the exit code for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a791681c-2ada-433e-8972-21af43374907">get_ExtendedTaskTerms</a>
</td>
<td align="left" width="63%">
Retrieves the application-defined extended terms for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3766023e-fd2b-471c-98bc-c77c3f71da5d">get_Id</a>
</td>
<td align="left" width="63%">
Retrieves the task identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b4ea726-4f65-4793-a809-6000ce1d4eed">get_IsExclusive</a>
</td>
<td align="left" width="63%">
Checks whether the node should be exclusively allocated to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caf813ef-c52b-4a72-8e2d-4cc4889df4fd">get_IsRerunnable</a>
</td>
<td align="left" width="63%">
Checks whether the task can be rerun after a failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/baeadb9c-906d-4c0f-8993-5dcba922f11e">get_MaximumNumberOfProcessors</a>
</td>
<td align="left" width="63%">
Retrieves the maximum number of processors required by the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff298b47-2a30-40db-b3dc-2e55d5cacae0">get_MinimumNumberOfProcessors</a>
</td>
<td align="left" width="63%">
Retrieves the minimum number of processors required by the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c3bdff6-0ff5-4a5e-b5e1-5ccf6930f6ad">get_Name</a>
</td>
<td align="left" width="63%">
Retrieves the display name of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fedeb5b-9430-4ccd-8e7f-d4cdc8585c31">get_ParentJobId</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the parent job.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c8ff00d-83dc-42bb-8c8f-ee075097e0ac">get_RequiredNodes</a>
</td>
<td align="left" width="63%">
Retrieves the list of required nodes for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/885f750a-d555-4e31-91de-ddb16e52a0bf">get_Runtime</a>
</td>
<td align="left" width="63%">
Retrieves the run-time limit for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d0c237f-c0ba-47fc-ac32-2b43cf03e74e">get_StartTime</a>
</td>
<td align="left" width="63%">
Retrieves the time that the task started running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5ee205f-09bc-4e96-9bfe-c805699b7716">get_Status</a>
</td>
<td align="left" width="63%">
Retrieves the task status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b325300c-a5b2-419d-87db-eef96527830a">get_Stderr</a>
</td>
<td align="left" width="63%">
Retrieves the file to which standard error has been redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e616c6a2-423f-4cfb-96ac-eab4fc4cea11">get_Stdin</a>
</td>
<td align="left" width="63%">
Retrieves the file from which standard input has been redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79e5ee7a-b210-4090-93d0-82d74b1c0096">get_Stdout</a>
</td>
<td align="left" width="63%">
Retrieves the file to which standard output has been redirected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d006b4f6-ced0-4c55-b9a8-eddce173da63">get_SubmitTime</a>
</td>
<td align="left" width="63%">
Retrieves the time that the task was submitted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/647e0431-f76f-4ce8-933a-563a9687b2e1">get_WorkDirectory</a>
</td>
<td align="left" width="63%">
Retrieves the startup directory for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afd50341-940f-4970-a5b7-7ac9251a3eb0">put_CommandLine</a>
</td>
<td align="left" width="63%">
Sets the command line for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce8aa776-d40a-4a61-a320-224a605b45a1">put_Depend</a>
</td>
<td align="left" width="63%">
Sets the dependent tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72737c55-c4c7-4493-b764-d946b41af091">put_IsExclusive</a>
</td>
<td align="left" width="63%">
Sets whether the node should be exclusively allocated to the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293f494a-e375-499c-9b46-925394b2762b">put_IsRerunnable</a>
</td>
<td align="left" width="63%">
Sets whether the task can be rerun after a failure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a4f884c-4789-4b93-8dd5-0ca28966eead">put_MaximumNumberOfProcessors</a>
</td>
<td align="left" width="63%">
Sets the maximum number of processors required by the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b5b338e-52af-44a2-9828-a41e67602986">put_MinimumNumberOfProcessors</a>
</td>
<td align="left" width="63%">
Sets the minimum number of processors required by the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f223ebad-a4bc-4177-8ac5-5419390fbc31">put_Name</a>
</td>
<td align="left" width="63%">
Sets the display name of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2a05786-fa4f-4e0e-b30d-f2391b081d6c">put_RequiredNodes</a>
</td>
<td align="left" width="63%">
Sets the list of required nodes for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78986f48-31ee-4699-b0a1-9877dfc4cfaa">put_Runtime</a>
</td>
<td align="left" width="63%">
Sets the run-time limit for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b80c4fc-ec41-44fc-887d-5663bebd7edb">put_Stderr</a>
</td>
<td align="left" width="63%">
Redirects standard error to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7fa3615-d6a9-4a73-bfbb-afe4035186d1">put_Stdin</a>
</td>
<td align="left" width="63%">
Redirects standard input to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/abeece55-2c5c-4335-b0ce-71cd9c432455">put_Stdout</a>
</td>
<td align="left" width="63%">
Redirects standard output to the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da34830b-62c0-484d-a20c-2800fd6dc05f">put_WorkDirectory</a>
</td>
<td align="left" width="63%">
Sets the startup directory for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04bcb160-5e8b-4364-b80b-b90a84f7ee9c">SetEnvironmentVariable</a>
</td>
<td align="left" width="63%">
Sets the task-specific environment variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4edf71ac-2a13-4e00-b554-bf003a0476d1">SetExtendedTaskTerm</a>
</td>
<td align="left" width="63%">
Sets the application-defined extended term for the task.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/12ee3ff7-ea46-43a3-9ee8-4b04ed88ac0d">CCP Interfaces</a>



<a href="https://msdn.microsoft.com/973ac354-175b-4497-9b02-46b8f9feabc4">Jobs and Tasks</a>
 

 

