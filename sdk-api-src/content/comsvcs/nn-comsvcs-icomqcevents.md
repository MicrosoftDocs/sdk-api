---
UID: NN:comsvcs.IComQCEvents
title: IComQCEvents
author: windows-sdk-content
description: Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue.
old-location: cos\icomqcevents.htm
tech.root: cossdk
ms.assetid: d7c8220d-a302-4f95-b0b6-8d47f9f27da7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComQCEvents, IComQCEvents interface [COM+], IComQCEvents interface [COM+],described, _dtc_IComQCEvents, comsvcs/IComQCEvents, cos.icomqcevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComQCEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComQCEvents interface


## -description


Notifies the subscriber if a queued message is created, de-queued, or moved to a retry or dead letter queue. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComQCEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComQCEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComQCEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54117583-4e8d-4ae9-8262-781f5f81636d">OnQCMoveToDeadQueue</a>
</td>
<td align="left" width="63%">
Generated when a message is moved to the dead letter queue and cannot be delivered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8f2af02-852d-4e36-9e0c-4919e2fba4a1">OnQCMoveToReTryQueue</a>
</td>
<td align="left" width="63%">
Generated when a message is moved to a queued components retry queue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cd9daf8-cc4d-4d48-b547-95b370f5a927">OnQCPlayback</a>
</td>
<td align="left" width="63%">
Generated when a messages contents are replayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dcd1726-650a-4bb5-ae12-48c6989e1692">OnQCQueueOpen</a>
</td>
<td align="left" width="63%">
Generated when a queued components queue is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4404fad-c656-4cbf-90d1-a09a7162a38f">OnQCReceive</a>
</td>
<td align="left" width="63%">
Generated when a message is successfully de-queued even though the queued components service might find something wrong with the contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21d685ce-b65f-4d13-b653-e6c6d1afa704">OnQCReceiveFail</a>
</td>
<td align="left" width="63%">
Generated when the receive message fails.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a7ff5ac-df0f-4aea-b6f1-813c7e22e6c2">OnQCRecord</a>
</td>
<td align="left" width="63%">
Generated when the queued components recorder creates the queued message.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>



<a href="https://msdn.microsoft.com/810305ad-c7fb-4627-8ca7-de37c5bef2f5">COM+ Queued Components</a>
 

 

