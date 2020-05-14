---
UID: NN:taskschd.ITriggerCollection
title: ITriggerCollection (taskschd.h)
description: Provides the methods that are used to add to, remove from, and get the triggers of a task.helpviewer_keywords: ["ITriggerCollection","ITriggerCollection interface [Task Scheduler]","ITriggerCollection interface [Task Scheduler]","described","taskschd.itriggercollection","taskschd/ITriggerCollection","triggers [Task Scheduler]","trigger collection interface"]
old-location: taskschd\itriggercollection.htm
tech.root: taskschd
ms.assetid: 5985ff67-3aa2-4ade-9d53-da4d640f5f6e
ms.date: 12/05/2018
ms.keywords: ITriggerCollection, ITriggerCollection interface [Task Scheduler], ITriggerCollection interface [Task Scheduler],described, taskschd.itriggercollection, taskschd/ITriggerCollection, triggers [Task Scheduler],trigger collection interface
f1_keywords:
- taskschd/ITriggerCollection
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
- ITriggerCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITriggerCollection interface


## -description


Provides the methods that are used to add to, remove from, and get the triggers of a task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITriggerCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITriggerCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITriggerCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears all triggers from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create">Create</a>
</td>
<td align="left" width="63%">
Creates a new trigger for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes the specified trigger from the collection of triggers used by the task.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITriggerCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection enumerator for this collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of triggers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the specified trigger from the collection.

</td>
</tr>
</table> 


## -remarks



When reading or writing XML for a task, the triggers for the task are specified in the <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/taskschedulerschema-triggers-tasktype-element">Triggers</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/daily-trigger-example--c---">Daily Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/weekly-trigger-example--c---">Weekly Trigger Example (C++)</a>, <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/logon-trigger-example--c---">Logon Trigger Example (C++)</a>, or <a href="https://docs.microsoft.com/windows/desktop/TaskSchd/boot-trigger-example--c---">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/taskschd/nn-taskschd-itrigger">ITrigger</a>



<a href="https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
 

 

