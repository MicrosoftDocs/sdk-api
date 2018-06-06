---
UID: NF:taskschd.IEventTrigger.put_Subscription
title: IEventTrigger::put_Subscription
author: windows-sdk-content
description: Gets or sets a query string that identifies the event that fires the trigger.
old-location: taskschd\ieventtrigger_subscription.htm
old-project: TaskSchd
ms.assetid: 884b98cd-f782-44af-9534-067198a7f48d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IEventTrigger interface [Task Scheduler],Subscription property, IEventTrigger.Subscription, IEventTrigger.put_Subscription, IEventTrigger::Subscription, IEventTrigger::get_Subscription, IEventTrigger::put_Subscription, Subscription property [Task Scheduler], Subscription property [Task Scheduler],IEventTrigger interface, put_Subscription, taskschd.ieventtrigger_subscription, taskschd/IEventTrigger::Subscription, taskschd/IEventTrigger::get_Subscription, taskschd/IEventTrigger::put_Subscription
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IEventTrigger.Subscription
 - IEventTrigger.get_Subscription
 - IEventTrigger.put_Subscription
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEventTrigger::put_Subscription


## -description


Gets or sets a query string that identifies the event that fires the trigger.

This property is read/write.


## -parameters


## -remarks



When reading or writing your own XML for a task, the event subscription is specified using the <a href="https://msdn.microsoft.com/ea351a55-c6f9-4e39-b15e-c2a1027a1360">Subscription</a> element of the Task Scheduler schema.

For more information about writing a query string for certain events, see <a href="http://go.microsoft.com/fwlink/p/?linkid=168218">Event Selection</a> and <a href="http://go.microsoft.com/fwlink/p/?linkid=168415">Subscribing to Events</a>.


#### Examples

The following query string defines a subscription to all level 2 events in the System channel.


<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>"&lt;QueryList&gt;
    &lt;Query Id='1'&gt;
        &lt;Select Path='System'&gt;*[System/Level=2]&lt;/Select&gt;
    &lt;/Query&gt;
&lt;/QueryList&gt;"</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

