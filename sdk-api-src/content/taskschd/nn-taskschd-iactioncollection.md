---
UID: NN:taskschd.IActionCollection
title: IActionCollection (taskschd.h)
author: windows-sdk-content
description: Contains the actions that are performed by the task.
old-location: taskschd\iactioncollection.htm
tech.root: taskschd
ms.assetid: aa7781b6-2600-4af5-95b8-2ac7928946fa
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActionCollection, IActionCollection interface [Task Scheduler], IActionCollection interface [Task Scheduler],described, actions [Task Scheduler],collection interface, taskschd.iactioncollection, taskschd/IActionCollection
ms.topic: interface
f1_keywords: 
 - "taskschd/IActionCollection"
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
 - IActionCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActionCollection interface


## -description


Contains the actions that are performed by the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IActionCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IActionCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears all the actions from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create">Create</a>
</td>
<td align="left" width="63%">
Creates and adds a new action to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a specified action from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection enumerator for the action collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_context">Context</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the identifier of the principal for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of actions in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a  specified action from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_xmltext">XmlText</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets an XML-formatted version of the collection.

</td>
</tr>
</table> 


## -remarks



When reading or writing XML for a task, the actions of the task are specified in the  <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-actions-tasktype-element">Actions</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

