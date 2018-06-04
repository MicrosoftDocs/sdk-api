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
 

 

