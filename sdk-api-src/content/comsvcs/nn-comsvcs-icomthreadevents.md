---
UID: NN:comsvcs.IComThreadEvents
title: IComThreadEvents
author: windows-sdk-content
description: Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated.
old-location: cos\icomthreadevents.htm
old-project: cossdk
ms.assetid: a6523088-cca4-41c1-a3fe-d8cb7320ff33
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], IComThreadEvents interface [COM+],described, _dtc_IComThreadEvents, comsvcs/IComThreadEvents, cos.icomthreadevents
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComThreadEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComThreadEvents interface


## -description


Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated. The subscriber is also notified if an activity is assigned or unassigned to an apartment thread. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComThreadEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComThreadEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComThreadEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2711b4b9-f27c-42c4-8f78-f31ffba2cfcf">OnThreadAssignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is assigned to an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d05c784a-5dcd-4155-baa0-775c499bd936">OnThreadBindToApartment</a>
</td>
<td align="left" width="63%">
Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9316965e-13e8-4e3a-9404-8e49334773bc">OnThreadStart</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8483962c-46c9-4ef1-8c7e-391a04334293">OnThreadTerminate</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c57b2427-9c39-4068-b531-9f18264746a1">OnThreadUnassignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is unassigned from an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21ce95a4-0e87-4e2d-a3fa-b21a079058e2">OnThreadUnBind</a>
</td>
<td align="left" width="63%">
Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

