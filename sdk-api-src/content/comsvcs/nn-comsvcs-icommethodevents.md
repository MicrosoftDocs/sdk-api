---
UID: NN:comsvcs.IComMethodEvents
title: IComMethodEvents
author: windows-sdk-content
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception.
old-location: cos\icommethodevents.htm
tech.root: cossdk
ms.assetid: 24670a23-4300-48f9-a089-dff3082cb544
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComMethodEvents, IComMethodEvents interface [COM+], IComMethodEvents interface [COM+],described, _dtc_IComMethodEvents, comsvcs/IComMethodEvents, cos.icommethodevents
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
 - IComMethodEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComMethodEvents interface


## -description


Notifies the subscriber if an object's method has been called, returned, or generated an exception. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComMethodEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComMethodEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComMethodEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d68fe2c-7032-46d2-b88d-0b4f81c74760">OnMethodCall</a>
</td>
<td align="left" width="63%">
Generated when an object's method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b504a2db-0d18-42f1-8572-dc066c3e7740">OnMethodException</a>
</td>
<td align="left" width="63%">
Generated when an object's method generates an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ade20bfc-0b50-4663-a1d3-14e2bd0c19a1">OnMethodReturn</a>
</td>
<td align="left" width="63%">
Generated when an object's method returns.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

