---
UID: NN:comsvcs.IComThreadEvents
title: IComThreadEvents
author: windows-sdk-content
description: Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated.
old-location: cos\icomthreadevents.htm
tech.root: cossdk
ms.assetid: a6523088-cca4-41c1-a3fe-d8cb7320ff33
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IComThreadEvents, IComThreadEvents interface [COM+], IComThreadEvents interface [COM+],described, _dtc_IComThreadEvents, comsvcs/IComThreadEvents, cos.icomthreadevents
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
 - IComThreadEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComThreadEvents interface


## -description


Notifies the subscriber if a single-threaded apartment (STA) is created or terminated, and when an apartment thread is allocated. The subscriber is also notified if an activity is assigned or unassigned to an apartment thread. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComThreadEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComThreadEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms679486(v=VS.85).aspx">OnThreadAssignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is assigned to an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686539(v=VS.85).aspx">OnThreadBindToApartment</a>
</td>
<td align="left" width="63%">
Generated when an apartment thread is allocated for a single-thread apartment (STA) thread that does not have an apartment thread to run in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684237(v=VS.85).aspx">OnThreadStart</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683567(v=VS.85).aspx">OnThreadTerminate</a>
</td>
<td align="left" width="63%">
Generated when a single-threaded apartment (STA) thread is terminated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686432(v=VS.85).aspx">OnThreadUnassignApartment</a>
</td>
<td align="left" width="63%">
Generated when an activity is unassigned from an apartment thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679255(v=VS.85).aspx">OnThreadUnBind</a>
</td>
<td align="left" width="63%">
Generated when the lifetime of the configured component is over and the activity count on the apartment thread can be decremented.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms681289(v=VS.85).aspx">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

