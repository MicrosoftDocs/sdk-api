---
UID: NN:comsvcs.IComUserEvent
title: IComUserEvent
author: windows-sdk-content
description: Notifies the subscriber of the specified user-defined metrics.
old-location: cos\icomuserevent.htm
tech.root: cossdk
ms.assetid: a443b54a-018f-48a0-b61c-9e18e9567a22
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComUserEvent, IComUserEvent interface [COM+], IComUserEvent interface [COM+],described, _dtc_IComUserEvent, comsvcs/IComUserEvent, cos.icomuserevent
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
 - IComUserEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComUserEvent interface


## -description


Notifies the subscriber of the specified user-defined metrics. The events are published to the subscriber using the <a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComUserEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComUserEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComUserEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c14bf53-7466-4cb0-b90f-681796e40fd3">OnUserEvent</a>
</td>
<td align="left" width="63%">
Provided for user components to generate user-defined events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1e0570ae-9099-465a-9133-72aa7d574932">COM+ Events</a>



<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>
 

 

