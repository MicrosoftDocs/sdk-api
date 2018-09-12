---
UID: NN:comsvcs.IComActivityEvents
title: IComActivityEvents
author: windows-sdk-content
description: Notifies the subscriber if an activity is created, destroyed, or timed out.
old-location: cos\icomactivityevents.htm
tech.root: cossdk
ms.assetid: 9b702bcd-d5a6-41fa-98ce-00a245dfe770
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IComActivityEvents, IComActivityEvents interface [COM+], IComActivityEvents interface [COM+],described, _dtc_IComActivityEvents, comsvcs/IComActivityEvents, cos.icomactivityevents
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
 - IComActivityEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComActivityEvents interface


## -description


Notifies the subscriber if an activity is created, destroyed, or timed out. The activity event is published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComActivityEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComActivityEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComActivityEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27d6dfd6-24c8-480b-9d91-6c6cce08384c">OnActivityCreate</a>
</td>
<td align="left" width="63%">
Generated when an activity starts.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af69bcf7-a925-42e2-a7a8-4ebf745955b9">OnActivityDestroy</a>
</td>
<td align="left" width="63%">
Generated when an activity is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5933798d-2208-4eab-8024-50236e5483a3">OnActivityEnter</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is entered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f39a8ce1-9c17-47eb-9405-c6a69dee88cc">OnActivityLeave</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is left.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a82fba1-a7d8-48d6-aa54-2f1a28e1b3d9">OnActivityLeaveSame</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is left after being entered recursively.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e055caab-379c-47c5-b62a-28ce5c2a0573">OnActivityReenter</a>
</td>
<td align="left" width="63%">
Generated when an activity thread is reentered recursively.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f097bea7-99a4-41eb-9518-834683d9402b">OnActivityTimeout</a>
</td>
<td align="left" width="63%">
Generated when a call into an activity times out.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

