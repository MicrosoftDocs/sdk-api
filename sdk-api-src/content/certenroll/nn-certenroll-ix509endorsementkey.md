---
UID: NN:certenroll.IX509EndorsementKey
title: IX509EndorsementKey
author: windows-sdk-content
description: X.509 Endorsement Key Interface
old-location: security\ix509endorsementkey.htm
tech.root: SecCertEnroll
ms.assetid: 24f063a7-02e3-47cf-89ca-ebc63bf3e2dc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509EndorsementKey, IX509EndorsementKey interface [Security], IX509EndorsementKey interface [Security],described, certenroll/IX509EndorsementKey, security.ix509endorsementkey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.dll
api_name:
 - IX509EndorsementKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EndorsementKey interface


## -description


X.509 Endorsement Key Interface


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EndorsementKey</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509EndorsementKey</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>IX509EndorsementKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379357(v=VS.85).aspx">AddCertificate</a>
</td>
<td align="left" width="63%">
Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379358(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379359(v=VS.85).aspx">ExportPublicKey</a>
</td>
<td align="left" width="63%">
Exports the endorsement public key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab1eb37a-d79e-4d02-8e60-6c093f42c68f">GetCertificateByIndex</a>
</td>
<td align="left" width="63%">
Gets the endorsement certificate associated with the endorsement key from the key storage provider for the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379361(v=VS.85).aspx">GetCertificateCount</a>
</td>
<td align="left" width="63%">
Gets the count of the endorsement certificates in the key storage provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379364(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn379368(v=VS.85).aspx">RemoveCertificate</a>
</td>
<td align="left" width="63%">
Removes an endorsement certificate related to the endorsement key from the key storage provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EndorsementKey</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Dn379362(v=VS.85).aspx">Length</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The bit length of the endorsement key. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Dn379365(v=VS.85).aspx">Opened</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/en-us/library/Dn379364(v=VS.85).aspx">Open</a> method has been successfully called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Dn379367(v=VS.85).aspx">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the encryption provider. The default is the Microsoft Platform Crypto Provider.

</td>
</tr>
</table> 

