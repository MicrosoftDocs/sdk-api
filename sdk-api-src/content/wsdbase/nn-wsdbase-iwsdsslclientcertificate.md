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

# IWSDSSLClientCertificate interface


## -description


Retrieves the client SSL certificate.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDSSLClientCertificate</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDSSLClientCertificate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDSSLClientCertificate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82f3f4ae-80fe-4382-9a22-00c70e99524f">GetClientCertificate</a>
</td>
<td align="left" width="63%">
Gets the client certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79dbd838-cffd-4571-8227-e508673c1b02">GetMappedAccessToken</a>
</td>
<td align="left" width="63%">
Gets the mapped access token.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href=" http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> method of <a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>.  If the connection did not arrive over SSL, the call to <a href=" http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> will return <b>E_NOINTERFACE</b>.

On the device host, the generated code calls the application's service method. This service method has access to the <a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a> interface through the <a href="https://msdn.microsoft.com/d8697474-bfe5-4704-b1ac-15cf96f2ca92">WSD_EVENT</a> structure. The <b>IWSDSSLClientCertificate</b> provides access to the client SSL certificate.



