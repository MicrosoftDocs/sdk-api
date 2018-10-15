---
UID: NS:wintrust._WIN_CERTIFICATE
title: "_WIN_CERTIFICATE"
author: windows-sdk-content
description: This structure encapsulates a signature used in verifying executable files.
old-location: security\win_certificate.htm
tech.root: seccrypto
ms.assetid: AC666871-265B-4D09-B7A6-DEC48D4645FD
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPWIN_CERTIFICATE, PWIN_CERTIFICATE, PWIN_CERTIFICATE structure pointer [Security], WIN_CERTIFICATE, WIN_CERTIFICATE structure [Security], _WIN_CERTIFICATE, security.win_certificate, wintrust/PWIN_CERTIFICATE, wintrust/WIN_CERTIFICATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wintrust.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WIN_CERTIFICATE
product: Windows
targetos: Windows
req.typenames: WIN_CERTIFICATE, *LPWIN_CERTIFICATE
req.redist: 
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

