---
UID: NN:taskschd.IRegisteredTask
title: IRegisteredTask (taskschd.h)
author: windows-sdk-content
description: Provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the properties that describe the task.
old-location: taskschd\iregisteredtask.htm
tech.root: taskschd
ms.assetid: 3743d012-ad7c-402f-8859-939bb01ee447
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRegisteredTask, IRegisteredTask interface [Task Scheduler], IRegisteredTask interface [Task Scheduler],described, taskschd.iregisteredtask, taskschd/IRegisteredTask
ms.topic: interface
f1_keywords: 
 - "taskschd/IRegisteredTask"
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
 - IRegisteredTask
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRegisteredTask interface


## -description


Provides the methods that are used to run the task immediately, get any running instances of the task, get or set the credentials that are used to register the task, and the  properties that describe the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredTask</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRegisteredTask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRegisteredTask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getinstances">GetInstances</a>
</td>
<td align="left" width="63%">
Returns all instances of the registered task that are currently running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getruntimes">GetRunTimes</a>
</td>
<td align="left" width="63%">
Gets the times that the registered task is scheduled to run during a specified time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-getsecuritydescriptor">GetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor that is used as credentials for the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run">Run</a>
</td>
<td align="left" width="63%">
Runs the registered task immediately.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex">RunEx</a>
</td>
<td align="left" width="63%">
Runs the registered task immediately using specified flags and a session identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor">SetSecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor that is used as credentials for the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops the registered task immediately.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRegisteredTask</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_definition">Definition</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the definition of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_enabled">Enabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a Boolean value that indicates if the registered task is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_lastruntime">LastRunTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the time the registered task was last run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_lasttaskresult">LastTaskResult</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the results that were returned the last time the registered task was run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_nextruntime">NextRunTime</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the time when the registered task is next scheduled to run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_numberofmissedruns">NumberOfMissedRuns</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of times the registered task has missed a scheduled run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_path">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the path to where the registered task is stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_state">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the operational state of the registered task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-get_xml">XML</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the XML-formatted registration information for the registered task.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

