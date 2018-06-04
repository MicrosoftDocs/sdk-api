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

# IInternalUnknown interface


## -description


Used exclusively in lightweight client-side handlers that require access to some of the internal interfaces on the proxy.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInternalUnknown</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IInternalUnknown</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInternalUnknown</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fa3478a-126c-43d9-851f-effa016c33f2">QueryInternalInterface</a>
</td>
<td align="left" width="63%">
Retrieves pointers to the supported internal interfaces on an object.

</td>
</tr>
</table> 


## -remarks



Handlers that need access to some of the internal interfaces on the proxy manager have to go through the <b>IInternalUnknown</b> interface. This prevents the handlers from blindly delegating and exposing the aggregatee's internal interfaces outside of the aggregate. These interfaces include <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a> and <a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a>. If the handler wants to expose <b>IClientSecurity</b> or <b>IMultiQI</b>, the handler should implement these interfaces itself and delegate to the proxy manager's implementation of these interfaces when appropriate.

For the <a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a> interface, if the client tries to set the security on an interface that the handler has exposed, the handler should set the security on the underlying network interface proxy.



For the <a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a> interface, the handler should fill in the interfaces it knows about and then forward the call to the proxy manager to fill in the rest of the interfaces.




## -see-also




<a href="https://msdn.microsoft.com/65066913-f9d8-48c7-bcb5-68c8ddc4a009">IClientSecurity</a>



<a href="https://msdn.microsoft.com/5e50396f-2931-403f-946a-dc096cb012cc">IMultiQI</a>



<a href="https://msdn.microsoft.com/b712237c-55d7-4f52-9cf6-19c6e5fb3182">Lightweight Client-Side Handler</a>
 

 

