---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICallInterceptor interface


## -description


Supports the registration and un-registering of event sinks wishing to be notified of calls made directly on the interface. In addition, this interface provides a means by which an invocation can be carried out with an indirect reference to the invocations arguments.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICallInterceptor</b> interface inherits from <b>ICallIndirect</b>. <b>ICallInterceptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICallInterceptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65f33bc3-9fcb-4ad5-908d-3ac06b9f8c6c">GetRegisteredSink</a>
</td>
<td align="left" width="63%">
Retrieves the registered event sink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07de2e42-0490-4801-8951-6e71ffb8ed93">RegisterSink</a>
</td>
<td align="left" width="63%">
Registers an event sink for receiving notifications of method calls.

</td>
</tr>
</table> 

