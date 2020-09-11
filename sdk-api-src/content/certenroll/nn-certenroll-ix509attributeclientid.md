---
UID: NN:certenroll.IX509AttributeClientId
title: IX509AttributeClientId (certenroll.h)
description: Represents an attribute that can be used to identify the client that generated a certificate request.
helpviewer_keywords: ["IX509AttributeClientId","IX509AttributeClientId interface [Security]","IX509AttributeClientId interface [Security]","described","certenroll/IX509AttributeClientId","security.ix509attributeclientid"]
old-location: security\ix509attributeclientid.htm
tech.root: security
ms.assetid: 82b773e3-7d47-4c85-a6b3-c8ef3e67630a
ms.date: 12/05/2018
ms.keywords: IX509AttributeClientId, IX509AttributeClientId interface [Security], IX509AttributeClientId interface [Security],described, certenroll/IX509AttributeClientId, security.ix509attributeclientid
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509AttributeClientId
 - certenroll/IX509AttributeClientId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeClientId
---

# IX509AttributeClientId interface


## -description

The <b>IX509AttributeClientId</b> interface represents an attribute that can be used to identify the client that generated a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a>. This can be used for post-mortem request analysis.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeClientId</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>. <b>IX509AttributeClientId</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509AttributeClientId</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://docs.microsoft.com/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-initializeencode">InitializeEncode</a>
</td>
<td align="left" width="63%">
Initializes the attribute from information about the user, client computer, and application that submitted the certificate request.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeClientId</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_clientid">ClientId</a>


</td>
<td align="left" width="63%">
Retrieves the type of client application that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_machinednsname">MachineDnsName</a>


</td>
<td align="left" width="63%">
Retrieves the Domain Name System (DNS) name of the computer that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_processname">ProcessName</a>


</td>
<td align="left" width="63%">
Retrieves the name of the application that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509attributeclientid-get_usersamname">UserSamName</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">Security Accounts Manager</a> (SAM) name of the user.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>

