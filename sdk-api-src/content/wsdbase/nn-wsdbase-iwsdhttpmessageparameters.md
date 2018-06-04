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

# IWSDHttpMessageParameters interface


## -description


Provides access to the HTTP headers used when transmitting messages via SOAP-over-HTTP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDHttpMessageParameters</b> interface inherits from <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>. <b>IWSDHttpMessageParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDHttpMessageParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Clears the HTTP headers used for SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff545736">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff546827">GetID</a>
</td>
<td align="left" width="63%">
Retrieves the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99b30444-1059-45c3-ac72-a0f98d722365">GetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c366773a-1869-4181-a457-560a1a9c84cd">GetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the current HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556644">SetContext</a>
</td>
<td align="left" width="63%">
Sets the private transmission context for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95a05239-f1d5-4bd8-8aec-1e641397caa0">SetID</a>
</td>
<td align="left" width="63%">
Sets the transport ID for the current transaction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd680016-1e6f-4d15-b1ca-cd2b6b210a71">SetInboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for incoming SOAP-over-HTTP transmissions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f54f86dc-4b25-4faa-8a37-b241e9ba8c6c">SetOutboundHttpHeaders</a>
</td>
<td align="left" width="63%">
Sets the HTTP headers used for outbound SOAP-over-HTTP transmissions.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

