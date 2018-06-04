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

# IWSDSignatureProperty interface


## -description


Provides properties of signed messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDSignatureProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWSDSignatureProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDSignatureProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5bab68b-8701-4258-bce2-9d3f8b850239">GetKeyInfo</a>
</td>
<td align="left" width="63%">
Gets the subject key ID of the certificate for a signed message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e13df6a4-f51f-4453-8482-563ff7c398c3">GetSignature</a>
</td>
<td align="left" width="63%">
Gets the signature of a message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95e34e7a-18d1-4402-bfd2-5f73d663c181">GetSignedInfoHash</a>
</td>
<td align="left" width="63%">
Gets the hash of a message signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b71ddd44-4823-455c-aea7-ee2f63b423bb">IsMessageSignatureTrusted</a>
</td>
<td align="left" width="63%">
Specifies if a message signature is trusted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca91bb1e-b8a6-4cfe-850c-887b39ae239e">IsMessageSigned</a>
</td>
<td align="left" width="63%">
Specifies if a message is signed.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href=" http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> method of <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a>.

<b>IWSDSignatureProperty</b> is useful to an application that wants to perform its own signature validation.  By passing a <b>NULL</b> to the <i>pConfigParam</i> of <a href="https://msdn.microsoft.com/dc757897-032c-4ea3-8f4e-cf00d4ec385b">WSDCreateDiscoveryProvider2</a>, the internal signature validation is disabled and the provider can perform its own validation by examining these properties.



