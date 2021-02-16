---
UID: NS:wincrypt._CERT_REQUEST_INFO
title: CERT_REQUEST_INFO (wincrypt.h)
description: The CERT_REQUEST_INFO structure contains information for a certificate request. The subject, subject public key, and attribute BLOBs are encoded.
helpviewer_keywords: ["*PCERT_REQUEST_INFO","CERT_REQUEST_INFO","CERT_REQUEST_INFO structure [Security]","CERT_V1","PCERT_REQUEST_INFO","PCERT_REQUEST_INFO structure pointer [Security]","_crypto2_cert_request_info","security.cert_request_info","wincrypt/CERT_REQUEST_INFO","wincrypt/PCERT_REQUEST_INFO"]
old-location: security\cert_request_info.htm
tech.root: security
ms.assetid: 6edeed33-16e1-4295-90e9-769929ab916a
ms.date: 12/05/2018
ms.keywords: '*PCERT_REQUEST_INFO, CERT_REQUEST_INFO, CERT_REQUEST_INFO structure [Security], CERT_V1, PCERT_REQUEST_INFO, PCERT_REQUEST_INFO structure pointer [Security], _crypto2_cert_request_info, security.cert_request_info, wincrypt/CERT_REQUEST_INFO, wincrypt/PCERT_REQUEST_INFO'
req.header: wincrypt.h
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
targetos: Windows
req.typenames: CERT_REQUEST_INFO, *PCERT_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REQUEST_INFO
 - wincrypt/_CERT_REQUEST_INFO
 - PCERT_REQUEST_INFO
 - wincrypt/PCERT_REQUEST_INFO
 - CERT_REQUEST_INFO
 - wincrypt/CERT_REQUEST_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_REQUEST_INFO
---

# CERT_REQUEST_INFO structure


## -description

The <b>CERT_REQUEST_INFO</b> structure contains information for a <a href="/windows/desktop/SecGloss/c-gly">certificate request</a>. The subject, subject <a href="/windows/desktop/SecGloss/p-gly">public key</a>, and <a href="/windows/desktop/SecGloss/a-gly">attribute BLOBs</a> are encoded.

## -struct-fields

### -field dwVersion

The certificate's version number. Defined version number is shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_V1"></a><a id="cert_v1"></a><dl>
<dt><b>CERT_V1</b></dt>
</dl>
</td>
<td width="60%">
version 1

</td>
</tr>
</table>

### -field Subject

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure that contains the certificate subject's encoded name.

### -field SubjectPublicKeyInfo

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure containing the encoded public key and its algorithm.

### -field cAttribute

Number of elements in the <b>rgAttribute</b> array.

### -field rgAttribute

A pointer to an array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a> structures, each holding attribute information about the certificate.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute">CRYPT_ATTRIBUTE</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencodecertificate">CryptSignAndEncodeCertificate</a>