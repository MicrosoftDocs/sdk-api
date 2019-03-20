---
UID: NN:taskschd.ITaskHandler
title: ITaskHandler (taskschd.h)
author: windows-sdk-content
description: Defines the methods that are called by the Task Scheduler service to manage a COM handler.
old-location: taskschd\itaskhandler.htm
tech.root: taskschd
ms.assetid: ea3100d7-a80b-4487-9786-24124f2d72f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITaskHandler, ITaskHandler interface [Task Scheduler], ITaskHandler interface [Task Scheduler],described, taskschd.itaskhandler, taskschd/ITaskHandler
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
 - ITaskHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskHandler interface


## -description


Defines the methods that are called by the Task Scheduler service to manage a COM handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITaskHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITaskHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITaskHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/851e3f20-a996-4a4b-bf10-7ba5c79c3d82">Pause</a>
</td>
<td align="left" width="63%">
Called to pause the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69e82100-2f21-49a1-8ede-e106cb8f1a25">Resume</a>
</td>
<td align="left" width="63%">
Called to restart the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0a51387-e638-40ee-a4e4-edd7f3115975">Start</a>
</td>
<td align="left" width="63%">
Required. Called to start the COM handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93a112e7-5e44-42a9-a5f5-d61e1ad1eabc">Stop</a>
</td>
<td align="left" width="63%">
Required. Called to stop the COM handler.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

