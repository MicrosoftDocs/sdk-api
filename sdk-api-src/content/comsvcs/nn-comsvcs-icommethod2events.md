---
UID: NN:comsvcs.IComMethod2Events
title: IComMethod2Events
author: windows-driver-content
description: Notifies the subscriber if an object's method has been called, returned, or generated an exception.
old-location: cos\icommethod2events.htm
old-project: cossdk
ms.assetid: e0642cb2-d5f2-4e4b-ad35-7818983ed467
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IComMethod2Events, IComMethod2Events interface [COM+], IComMethod2Events interface [COM+], described, _dtc_IComMethod2Events, comsvcs/IComMethod2Events, cos.icommethod2events
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IComMethod2Events
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IComMethod2Events interface


## -description


Notifies the subscriber if an object's method has been called, returned, or generated an exception. This interface extends the <a href="https://msdn.microsoft.com/24670a23-4300-48f9-a089-dff3082cb544">IComMethodEvents</a> interface to provide thread information. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComMethod2Events</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComMethod2Events</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComMethod2Events</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a209526-f548-404b-9d82-f52cfe89a4f8">OnMethodCall2</a>
</td>
<td align="left" width="63%">
Generated when an object's method is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a797a578-2d0d-45f0-820a-2616f6c65a42">OnMethodException2</a>
</td>
<td align="left" width="63%">
Generated when an object's method generates an exception.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf5a7b69-a794-4497-99c9-20c41d454753">OnMethodReturn2</a>
</td>
<td align="left" width="63%">
Generated when an object's method returns.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

