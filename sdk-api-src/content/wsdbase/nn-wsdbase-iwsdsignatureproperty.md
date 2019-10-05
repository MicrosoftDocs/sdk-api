---
UID: NN:wsdbase.IWSDSignatureProperty
title: IWSDSignatureProperty (wsdbase.h)
author: windows-sdk-content
description: Provides properties of signed messages.
old-location: ncd\iwsdsignatureproperty.htm
tech.root: WsdApi
ms.assetid: 10e95100-4890-4c00-b231-bb7125fed197
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDSignatureProperty, IWSDSignatureProperty interface, IWSDSignatureProperty interface,described, ncd.iwsdsignatureproperty, wsdbase/IWSDSignatureProperty
ms.topic: interface
f1_keywords: 
 - "wsdbase/IWSDSignatureProperty"
dev_langs:
 - c++
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSignatureProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDSignatureProperty interface


## -description


Provides properties of signed messages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDSignatureProperty</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWSDSignatureProperty</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd379728(v=vs.85)">GetKeyInfo</a>
</td>
<td align="left" width="63%">
Gets the subject key ID of the certificate for a signed message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsignatureproperty-getsignature">GetSignature</a>
</td>
<td align="left" width="63%">
Gets the signature of a message.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsignatureproperty-getsignedinfohash">GetSignedInfoHash</a>
</td>
<td align="left" width="63%">
Gets the hash of a message signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsignatureproperty-ismessagesignaturetrusted">IsMessageSignatureTrusted</a>
</td>
<td align="left" width="63%">
Specifies if a message signature is trusted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nf-wsdbase-iwsdsignatureproperty-ismessagesigned">IsMessageSigned</a>
</td>
<td align="left" width="63%">
Specifies if a message is signed.

</td>
</tr>
</table> 


## -remarks



An application can acquire this interface by calling the <a href="http://go.microsoft.com/fwlink/p/?linkid=22407">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nn-wsddisco-iwsdiscoveredservice">IWSDiscoveredService</a>.

<b>IWSDSignatureProperty</b> is useful to an application that wants to perform its own signature validation.  By passing a <b>NULL</b> to the <i>pConfigParam</i> of <a href="https://docs.microsoft.com/windows/desktop/api/wsddisco/nf-wsddisco-wsdcreatediscoveryprovider2">WSDCreateDiscoveryProvider2</a>, the internal signature validation is disabled and the provider can perform its own validation by examining these properties.



