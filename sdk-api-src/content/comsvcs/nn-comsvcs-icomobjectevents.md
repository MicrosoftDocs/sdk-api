---
UID: NN:comsvcs.IComObjectEvents
title: IComObjectEvents
author: windows-sdk-content
description: Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed.
old-location: cos\icomobjectevents.htm
tech.root: cossdk
ms.assetid: 4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComObjectEvents, IComObjectEvents interface [COM+], IComObjectEvents interface [COM+],described, _dtc_IComObjectEvents, comsvcs/IComObjectEvents, cos.icomobjectevents
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IComObjectEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComObjectEvents interface


## -description


Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed. The subscriber is notified if <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">IObjectContext::DisableCommit</a>, <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">IObjectContext::EnableCommit</a>, <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">IObjectContext::SetComplete</a> or <a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">IObjectContext::SetAbort</a> is called. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComObjectEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComObjectEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/413d7216-294c-4e46-b24c-abe1d1a09239">OnDisableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/e83d1223-9b8e-4a92-b98d-9d2b6ed34721">DisableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88fdf857-1dbd-4a6b-87c6-0d72eeeab9b4">OnEnableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/6571aadc-bf5a-48c3-817a-66ce444ef96a">EnableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/149e3820-0d5b-46ee-9be9-22850115a7c7">OnObjectActivate</a>
</td>
<td align="left" width="63%">
Generated when an object gets an instance of a new JIT-activated object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3284da44-bcc4-49eb-9aa8-40061bf51869">OnObjectDeactivate</a>
</td>
<td align="left" width="63%">
Generated when the JIT-activated object is freed by <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a> or <a href="https://msdn.microsoft.com/c254305f-1fc5-417e-b93b-d5e2b36e9e39">SetAbort</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bda05b7-3306-428c-b920-d87eee0b35d7">OnSetComplete</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/8ff25b68-fcb3-4e11-9c74-b49b31806796">SetComplete</a> on a context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

