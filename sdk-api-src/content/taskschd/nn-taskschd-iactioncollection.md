---
UID: NN:taskschd.IActionCollection
title: IActionCollection
author: windows-sdk-content
description: Contains the actions that are performed by the task.
old-location: taskschd\iactioncollection.htm
tech.root: TaskSchd
ms.assetid: aa7781b6-2600-4af5-95b8-2ac7928946fa
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IActionCollection, IActionCollection interface [Task Scheduler], IActionCollection interface [Task Scheduler],described, actions [Task Scheduler],collection interface, taskschd.iactioncollection, taskschd/IActionCollection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IActionCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActionCollection interface


## -description


Contains the actions that are performed by the task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActionCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IActionCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/59a1c49d-01e0-4331-997a-deb5d45d5766">Clear</a>
</td>
<td align="left" width="63%">
Clears all the actions from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/815a000b-ba02-470d-80e6-06ba3c8ea014">Create</a>
</td>
<td align="left" width="63%">
Creates and adds a new action to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91332ec0-8225-421a-baae-1a106be157a9">Remove</a>
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

<a href="https://msdn.microsoft.com/09d8924e-5153-4911-9662-93f71e39e583">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/e365955e-1648-4e11-b602-016dcbeb129e">Context</a>


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

<a href="https://msdn.microsoft.com/c9d11aa9-c182-4633-9fc6-d9cf53adc25a">Count</a>


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

<a href="https://msdn.microsoft.com/70d9cc9f-c539-4a5a-8b29-ca4d7464ab3f">Item</a>


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

<a href="https://msdn.microsoft.com/1c72546d-26e3-441c-875c-a41078ded0b7">XmlText</a>


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



When reading or writing XML for a task, the actions of the task are specified in the  <a href="https://msdn.microsoft.com/0a48fbd6-8a6f-4bad-9b28-0631dce15748">Actions</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/7c70b743-aff2-4ef5-b65b-ef0b5fdacade">Weekly Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/15647234-8d1f-4d75-b215-92927b300c1f">Logon Trigger Example (C++)</a>, or <a href="https://msdn.microsoft.com/d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

