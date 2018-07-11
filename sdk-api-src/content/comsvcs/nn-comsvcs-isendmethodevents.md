---
UID: NN:comsvcs.ISendMethodEvents
title: ISendMethodEvents
author: windows-sdk-content
description: Describes an event class that notifies subscribers whenever a method on the object that implements it either is called or returns from a call.
old-location: cos\isendmethodevents.htm
old-project: cossdk
ms.assetid: d1437581-8a2b-4e88-aa12-a16eb9f40125
ms.author: windowssdkdev
ms.date: 06/18/2018
ms.keywords: ISendMethodEvents, ISendMethodEvents interface [COM+], ISendMethodEvents interface [COM+],described, _cos_ISendMethodEvents, comsvcs/ISendMethodEvents, cos.isendmethodevents
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
 - ISendMethodEvents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ISendMethodEvents interface


## -description


Describes an event class that notifies subscribers whenever a method on the object that implements it either is called or returns from a call. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISendMethodEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISendMethodEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISendMethodEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/730466c8-440c-42ee-899f-0d93007fbf8d">SendMethodCall</a>
</td>
<td align="left" width="63%">
Generated when a method is called through a component interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9c8a680-644a-4617-866f-36e721bbc7aa">SendMethodReturn</a>
</td>
<td align="left" width="63%">
Generated when a method called through a component interface returns control to the caller.

</td>
</tr>
</table> 


## -remarks



To send method events to the COM+ tracker property, you need to obtain a handle to it and you need to obtain its GUID, which is defined as follows.

<pre class="syntax" xml:space="preserve"><code>GUID guidTrkPropPolicy = {0xecabaeb3, 0x7f19, 0x11d2, {0x97, 0x8e, 0x00, 0x00, 0xf8, 0x75, 0x7e, 0x2a}}
</code></pre>
To obtain a handle to the COM+ tracker property, call the <a href="https://msdn.microsoft.com/76c6f790-9103-4cee-8a67-0f69b00ba0a1">IContext::GetProperty</a> method with the <i>rGuid</i> argument set equal to this GUID.




## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>
 

 

