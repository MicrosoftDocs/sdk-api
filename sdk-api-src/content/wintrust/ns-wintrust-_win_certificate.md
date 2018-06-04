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

# _WIN_CERTIFICATE structure


## -description


This structure encapsulates a signature used in verifying executable files.


## -struct-fields




### -field dwLength

Specifies the length, in bytes, of the signature.


### -field wRevision

Specifies the certificate revision.

The only defined certificate revision is <b>WIN_CERT_REVISION_1_0 (0x0100)</b>.


### -field wCertificateType

Specifies the type of certificate.

<table>
<tr>
<th>Value </th>
<th>Description </th>
</tr>
<tr>
<td>WIN_CERT_TYPE_X509 (0x0001)</td>
<td>The <i>bCertificate</i> member contains an X.509 certificate.</td>
</tr>
<tr>
<td>WIN_CERT_TYPE_PKCS_SIGNED_DATA (0x0002)</td>
<td>The <i>bCertificate</i> member contains a PKCS <b>SignedData</b> structure.</td>
</tr>
<tr>
<td>WIN_CERT_TYPE_RESERVED_1 (0x0003)</td>
<td>Reserved.</td>
</tr>
<tr>
<td>WIN_CERT_TYPE_PKCS1_SIGN (0x0009)</td>
<td>The <i>bCertificate</i> member contains <b>PKCS1_MODULE_SIGN</b> fields.</td>
</tr>
</table>
 


### -field bCertificate

An array of certificates.

The format of this member depends on the value of <i>wCertificateType</i>.

