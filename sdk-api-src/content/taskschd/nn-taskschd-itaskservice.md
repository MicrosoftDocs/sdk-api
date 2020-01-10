---
UID: NN:taskschd.ITaskService
title: ITaskService (taskschd.h)
description: Provides access to the Task Scheduler service for managing registered tasks.
old-location: taskschd\itaskservice.htm
tech.root: taskschd
ms.assetid: 2459aaae-4c3a-458a-ad2c-bfff3a0322d3
ms.date: 12/05/2018
ms.keywords: ITaskService, ITaskService interface [Task Scheduler], ITaskService interface [Task Scheduler],described, taskschd.itaskservice, taskschd/ITaskService
f1_keywords:
- taskschd/ITaskService
dev_langs:
- c++
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
- ITaskService
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITaskService interface


## -description


Provides access to the Task Scheduler service for managing registered tasks.

The <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect">ITaskService::Connect</a> method should be called before calling any of the other <b>ITaskService</b> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskService</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITaskService</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITaskService</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects to a remote machine and associates all subsequent calls on this interface with a remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the path to a  folder of registered tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks">GetRunningTasks</a>
</td>
<td align="left" width="63%">
Gets a collection of running tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask">NewTask</a>
</td>
<td align="left" width="63%">
Returns an empty task definition object to be filled in with settings and properties and then registered using the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition">ITaskFolder::RegisterTaskDefinition</a> method.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskService</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_connected">Connected</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates if you are connected to the Task Scheduler service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_connecteddomain">ConnectedDomain</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the domain to which the <a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_targetserver">TargetServer</a> computer is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_connecteduser">ConnectedUser</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the user that is connected to the Task Scheduler service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_highestversion">HighestVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the highest version of Task Scheduler that a computer supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itaskservice-get_targetserver">TargetServer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the computer that is running the Task Scheduler service that the user is connected to.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

