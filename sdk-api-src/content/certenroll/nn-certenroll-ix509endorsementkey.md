---
UID: NN:certenroll.IX509EndorsementKey
title: IX509EndorsementKey
author: windows-sdk-content
description: X.509 Endorsement Key Interface
old-location: security\ix509endorsementkey.htm
tech.root: seccertenroll
ms.assetid: 24f063a7-02e3-47cf-89ca-ebc63bf3e2dc
ms.author: windowssdkdev
ms.date: 12/5/2018
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509EndorsementKey</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IX509EndorsementKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://msdn.microsoft.com/24621d53-c435-43e9-b709-619908f09f3b">AddCertificate</a>
</td>
<td align="left" width="63%">
Add an endorsement key certificate to the key storage provider (KSP) that supports endorsement keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71855c96-a828-4bb6-849a-53be8269277d">Close</a>
</td>
<td align="left" width="63%">
Closes the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b38c6421-2918-4d0e-81ed-d9d575817efa">ExportPublicKey</a>
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
<a href="https://msdn.microsoft.com/1a8ae8f9-c4df-4701-845d-7f9a42593d57">GetCertificateCount</a>
</td>
<td align="left" width="63%">
Gets the count of the endorsement certificates in the key storage provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06855fc0-0d87-4fe7-9525-55eb60bffcd1">Open</a>
</td>
<td align="left" width="63%">
Opens the endorsement key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40c5d77c-9b0d-4ee4-a02e-cec9b2f1b392">RemoveCertificate</a>
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

<a href="https://msdn.microsoft.com/31a94a37-ab56-4cb5-b4e0-ab3c74b748a0">Length</a>


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

<a href="https://msdn.microsoft.com/6bc1030b-66c9-4175-a3bb-6194d039c73f">Opened</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/06855fc0-0d87-4fe7-9525-55eb60bffcd1">Open</a> method has been successfully called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5031d14d-8a10-4821-aed4-b49e12027d91">ProviderName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
The name of the encryption provider. The default is the Microsoft Platform Crypto Provider.

</td>
</tr>
</table> 

