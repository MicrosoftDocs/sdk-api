---
UID: NS:wincrypt._CERT_OR_CRL_BLOB
title: CERT_OR_CRL_BLOB (wincrypt.h)
author: windows-sdk-content
description: Encapsulates certificates for use with Internet Key Exchange messages.
old-location: security\cert_or_crl_blob.htm
tech.root: SecCrypto
ms.assetid: f1e37c8f-7fca-4bf1-868f-8ec03a23a434
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_OR_CRL_BLOB, CERT_BUNDLE_CERTIFICATE, CERT_BUNDLE_CRL, CERT_OR_CRL_BLOB, CERT_OR_CRL_BLOB structure [Security], PCERT_OR_CRL_BLOB, PCERT_OR_CRL_BLOB structure pointer [Security], security.cert_or_crl_blob, wincrypt/CERT_OR_CRL_BLOB, wincrypt/PCERT_OR_CRL_BLOB"
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - CERT_OR_CRL_BLOB
product: Windows
targetos: Windows
req.typenames: CERT_OR_CRL_BLOB, *PCERT_OR_CRL_BLOB
req.redist: 
ms.custom: 19H1
---

# CERT_OR_CRL_BLOB structure


## -description


The <b>CERT_OR_CRL_BLOB</b> structure encapsulates certificates for use with Internet Key Exchange messages.


## -struct-fields




### -field dwChoice

A <b>DWORD</b> value that specifies the content type of the buffer pointed to by the <b>pbEncoded</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_BUNDLE_CERTIFICATE"></a><a id="cert_bundle_certificate"></a><dl>
<dt><b>CERT_BUNDLE_CERTIFICATE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <b>pbEncoded</b> member points to an encoded certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_BUNDLE_CRL"></a><a id="cert_bundle_crl"></a><dl>
<dt><b>CERT_BUNDLE_CRL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The <b>pbEncoded</b> member points to a certificate list.

</td>
</tr>
</table>
 


### -field cbEncoded

The size, in bytes, of the buffer pointed to by the <b>pbEncoded</b> member.


### -field pbEncoded

A pointer to a buffer that contains a certificate or a <a href="https://msdn.microsoft.com/a06e71b4-63c7-4d4a-820c-e5901015aaa6">CERT_OR_CRL_BUNDLE</a> structure that contains an array of certificates as specified by the <b>dwChoice</b> member. 

