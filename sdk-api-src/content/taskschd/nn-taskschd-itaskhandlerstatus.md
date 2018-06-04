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

# ITaskHandlerStatus interface


## -description


Provides the methods that are used by COM handlers to notify the Task Scheduler about the status of the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskHandlerStatus</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskHandlerStatus</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskHandlerStatus</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6f7adf5-3cdb-4691-bc0a-682df7f019e2">TaskCompleted</a>
</td>
<td align="left" width="63%">
Tells the Task Scheduler that the COM handler is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cab2b3b-7293-4d06-843f-9151d62d4950">UpdateStatus</a>
</td>
<td align="left" width="63%">
Tells the Task Scheduler about the percentage of completion of the COM handler.

</td>
</tr>
</table> 


## -remarks



For information on specifying a COM handler action, see the <a href="https://msdn.microsoft.com/fb5cc2c3-ba86-401a-b51f-b28d1f5be58f">IComHandlerAction</a> interface.

For information on the required interfaces that must be implemented by the handler, see the  <a href="https://msdn.microsoft.com/ea3100d7-a80b-4487-9786-24124f2d72f1">ITaskHandler</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

