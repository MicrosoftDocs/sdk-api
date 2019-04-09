---
UID: NN:taskschd.ITriggerCollection
title: ITriggerCollection (taskschd.h)
author: windows-sdk-content
description: Provides the methods that are used to add to, remove from, and get the triggers of a task.
old-location: taskschd\itriggercollection.htm
tech.root: taskschd
ms.assetid: 5985ff67-3aa2-4ade-9d53-da4d640f5f6e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITriggerCollection, ITriggerCollection interface [Task Scheduler], ITriggerCollection interface [Task Scheduler],described, taskschd.itriggercollection, taskschd/ITriggerCollection, triggers [Task Scheduler],trigger collection interface
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
 - ITriggerCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITriggerCollection interface


## -description


Provides the methods that are used to add to, remove from, and get the triggers of a task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITriggerCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITriggerCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/9a15ed27-a381-4b5c-9725-3a55ce86d666">Clear</a>
</td>
<td align="left" width="63%">
Clears all triggers from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70780fca-ba97-42b8-bc00-867c2761953c">Create</a>
</td>
<td align="left" width="63%">
Creates a new trigger for the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af3e04e6-20ec-412b-a0d2-41d31137dfca">Remove</a>
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

<a href="https://msdn.microsoft.com/a5df593a-8771-4a96-a9dd-abd4e3f1721f">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/ae4ff1b8-f030-420b-b96a-b5c1246c04ce">Count</a>


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

<a href="https://msdn.microsoft.com/007e5792-bb91-435f-abe9-27366e6ec58a">Item</a>


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



When reading or writing XML for a task, the triggers for the task are specified in the <a href="https://msdn.microsoft.com/4bf8e85e-3742-433d-821f-736fb2ff7139">Triggers</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/7c70b743-aff2-4ef5-b65b-ef0b5fdacade">Weekly Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/15647234-8d1f-4d75-b215-92927b300c1f">Logon Trigger Example (C++)</a>, or <a href="https://msdn.microsoft.com/d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/165297c1-704b-4ab3-a9e3-4aa3f10e07b1">ITrigger</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

