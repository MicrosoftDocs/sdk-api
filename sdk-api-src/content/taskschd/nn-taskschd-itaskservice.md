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

# ITaskService interface


## -description


Provides access to the Task Scheduler service for managing registered tasks.

The <a href="https://msdn.microsoft.com/ba810bac-e587-4eb8-871c-449b4174ab46">ITaskService::Connect</a> method should be called before calling any of the other <b>ITaskService</b> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskService</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskService</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ba810bac-e587-4eb8-871c-449b4174ab46">Connect</a>
</td>
<td align="left" width="63%">
Connects to a remote machine and associates all subsequent calls on this interface with a remote session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/144b070f-43e9-40d6-8461-832abc7facd3">GetFolder</a>
</td>
<td align="left" width="63%">
Gets the path to a  folder of registered tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6248cf51-acd8-4317-9837-99dcf918e816">GetRunningTasks</a>
</td>
<td align="left" width="63%">
Gets a collection of running tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/821fc610-cf94-4548-950d-b4fd7b2f90dc">NewTask</a>
</td>
<td align="left" width="63%">
Returns an empty task definition object to be filled in with settings and properties and then registered using the <a href="https://msdn.microsoft.com/a94db861-b24e-476a-810d-2cf3bbfc67d1">ITaskFolder::RegisterTaskDefinition</a> method.

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

<a href="https://msdn.microsoft.com/51450195-f11a-469a-a98f-4d1e00343e41">Connected</a>


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

<a href="https://msdn.microsoft.com/13a67d82-f239-450c-9490-02f07e672a64">ConnectedDomain</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the domain to which the <a href="https://msdn.microsoft.com/2b8c55d7-72e2-4b75-8850-3f042ba83c60">TargetServer</a> computer is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2fdff427-a363-4ce2-b1fe-a1ed945cae8b">ConnectedUser</a>


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

<a href="https://msdn.microsoft.com/27b08a17-fdd9-4c28-b498-e10e80ae49f0">HighestVersion</a>


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

<a href="https://msdn.microsoft.com/2b8c55d7-72e2-4b75-8850-3f042ba83c60">TargetServer</a>


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




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

