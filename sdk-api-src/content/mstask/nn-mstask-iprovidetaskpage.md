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

# IProvideTaskPage interface


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

Provides the methods to access the property sheet settings of a task.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProvideTaskPage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProvideTaskPage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProvideTaskPage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2313abc1-587f-473b-8d2e-390dfa7234ab">GetPage</a>
</td>
<td align="left" width="63%">
Retrieves the property sheet pages associated with a task.

</td>
</tr>
</table> 


## -remarks



This is the primary interface of the <a href="t.htm">task object</a>. To create a task object, call 
<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a> for existing tasks or 
<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">ITaskScheduler::NewWorkItem</a> for new tasks.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/f234f5b3-d668-44c3-8d03-c333cfe3acde">C/C++ Code Example: Retrieving a Task Page</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/27391e34-8632-4ab5-9d6e-d2fde7942f80">ITaskScheduler::Activate</a>



<a href="https://msdn.microsoft.com/1fbd65ae-0b54-4175-bf26-4226b1aabdc1">ITaskScheduler::NewWorkItem</a>
 

 

