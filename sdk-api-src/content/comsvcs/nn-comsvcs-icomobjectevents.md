---
UID: NN:comsvcs.IComObjectEvents
title: IComObjectEvents
author: windows-sdk-content
description: Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed.
old-location: cos\icomobjectevents.htm
old-project: cossdk
ms.assetid: 4354fc5b-4d72-4a56-b246-2ae2cf9b5ae1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IComObjectEvents, IComObjectEvents interface [COM+], IComObjectEvents interface [COM+],described, _dtc_IComObjectEvents, comsvcs/IComObjectEvents, cos.icomobjectevents
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
 - IComObjectEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComObjectEvents interface


## -description


Notifies the subscriber if an instance of a just-in-time (JIT) activated object has been created or freed. The subscriber is notified if <a href="https://msdn.microsoft.com/en-us/library/ms687629(v=VS.85).aspx">IObjectContext::DisableCommit</a>, <a href="https://msdn.microsoft.com/en-us/library/ms681803(v=VS.85).aspx">IObjectContext::EnableCommit</a>, <a href="https://msdn.microsoft.com/en-us/library/ms684201(v=VS.85).aspx">IObjectContext::SetComplete</a> or <a href="https://msdn.microsoft.com/en-us/library/ms686120(v=VS.85).aspx">IObjectContext::SetAbort</a> is called. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComObjectEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IComObjectEvents</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms680606(v=VS.85).aspx">OnDisableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/en-us/library/ms687629(v=VS.85).aspx">DisableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683628(v=VS.85).aspx">OnEnableCommit</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/en-us/library/ms681803(v=VS.85).aspx">EnableCommit</a> on a context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679174(v=VS.85).aspx">OnObjectActivate</a>
</td>
<td align="left" width="63%">
Generated when an object gets an instance of a new JIT-activated object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679569(v=VS.85).aspx">OnObjectDeactivate</a>
</td>
<td align="left" width="63%">
Generated when the JIT-activated object is freed by <a href="https://msdn.microsoft.com/en-us/library/ms684201(v=VS.85).aspx">SetComplete</a> or <a href="https://msdn.microsoft.com/en-us/library/ms686120(v=VS.85).aspx">SetAbort</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680204(v=VS.85).aspx">OnSetComplete</a>
</td>
<td align="left" width="63%">
Generated when the client calls <a href="https://msdn.microsoft.com/en-us/library/ms684201(v=VS.85).aspx">SetComplete</a> on a context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

