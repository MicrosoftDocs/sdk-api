---
UID: NN:taskschd.IRunningTask
title: IRunningTask (taskschd.h)
author: windows-sdk-content
description: Provides the methods to get information from and control a running task.
old-location: taskschd\irunningtask.htm
tech.root: taskschd
ms.assetid: 71a06a8f-8628-415d-b002-977c0d27f9a4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRunningTask, IRunningTask interface [Task Scheduler], IRunningTask interface [Task Scheduler],described, taskschd.irunningtask, taskschd/IRunningTask
ms.topic: interface
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
 - IRunningTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRunningTask interface


## -description


Provides the methods to get information from and control a running task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunningTask</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRunningTask</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IRunningTask</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f46d82ff-2f1b-477b-b043-665659ad8982">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes all of the local instance variables of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fdf325f-5652-42b0-99e3-3950dba1ef11">Stop</a>
</td>
<td align="left" width="63%">
Stops this instance of the task.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRunningTask</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/52b58477-e968-4c76-835d-02ed63cef641">CurrentAction</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the current action that the running task is performing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/933a0e41-e025-483a-98c4-a3b8e264c462">EnginePID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the process ID for the engine (process) which is running the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/993682d1-c77c-48d8-bec6-aab810c8bcda">InstanceGuid</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the GUID identifier for this instance of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/26938b6c-9c83-4065-9714-6bd0d187c7f1">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the name of the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8c364628-63dd-4018-9eeb-6acab265c144">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the path to where the task is stored.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/50a1d81d-9762-4d1f-801a-b2c54ad9c5bc">State</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the state of the running task.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b237ddd-e4e8-47f7-97e7-360e79841acc">IRegisteredTask::Run</a>



<a href="https://msdn.microsoft.com/d6d09ab1-026d-4ee9-b520-c7702e37504e">IRegisteredTask::RunEx</a>



<a href="https://msdn.microsoft.com/f95efba5-563d-49c0-81d3-143aa158ad8f">IRunningTaskCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

