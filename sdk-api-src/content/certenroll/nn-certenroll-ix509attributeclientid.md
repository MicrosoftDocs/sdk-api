---
UID: NN:certenroll.IX509AttributeClientId
title: IX509AttributeClientId
author: windows-sdk-content
description: Represents an attribute that can be used to identify the client that generated a certificate request.
old-location: security\ix509attributeclientid.htm
old-project: seccertenroll
ms.assetid: 82b773e3-7d47-4c85-a6b3-c8ef3e67630a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509AttributeClientId, IX509AttributeClientId interface [Security], IX509AttributeClientId interface [Security],described, certenroll/IX509AttributeClientId, security.ix509attributeclientid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509AttributeClientId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeClientId interface


## -description


The <b>IX509AttributeClientId</b> interface represents an attribute that can be used to identify the client that generated a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>. This can be used for post-mortem request analysis.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509AttributeClientId</b> interface inherits from <a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>. <b>IX509AttributeClientId</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/653b44fd-f69c-49e3-8aee-02445fa03cde">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a  <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded byte array that contains the attribute value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a0e5b6f-0522-4c60-9ea1-7a5c2722cebd">InitializeEncode</a>
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

<a href="https://msdn.microsoft.com/43073f84-28c6-4342-82ec-ca2289d51e02">ClientId</a>


</td>
<td align="left" width="63%">
Retrieves the type of client application that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/596682fc-aaf4-4247-a44b-34001cf7aecb">MachineDnsName</a>


</td>
<td align="left" width="63%">
Retrieves the Domain Name System (DNS) name of the computer that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7e273ffe-3f80-49b6-a4e5-939f5ba9d5bd">ProcessName</a>


</td>
<td align="left" width="63%">
Retrieves the name of the application that generated the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a5a5027f-3854-4064-9cf7-675562b4cd57">UserSamName</a>


</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) name of the user.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/20965768-2c6b-488a-ab7c-5e0f6f28ac9b">IX509Attribute</a>
 

 

