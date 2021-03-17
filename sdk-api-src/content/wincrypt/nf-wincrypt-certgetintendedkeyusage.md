---
UID: NF:wincrypt.CertGetIntendedKeyUsage
title: CertGetIntendedKeyUsage function (wincrypt.h)
description: Acquires the intended key usage bytes from a certificate.
helpviewer_keywords: ["CertGetIntendedKeyUsage","CertGetIntendedKeyUsage function [Security]","_crypto2_certgetintendedkeyusage","security.certgetintendedkeyusage","wincrypt/CertGetIntendedKeyUsage"]
old-location: security\certgetintendedkeyusage.htm
tech.root: security
ms.assetid: d09c3626-f864-4774-8511-3e912f62e520
ms.date: 12/05/2018
ms.keywords: CertGetIntendedKeyUsage, CertGetIntendedKeyUsage function [Security], _crypto2_certgetintendedkeyusage, security.certgetintendedkeyusage, wincrypt/CertGetIntendedKeyUsage
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertGetIntendedKeyUsage
 - wincrypt/CertGetIntendedKeyUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetIntendedKeyUsage
---

# CertGetIntendedKeyUsage function


## -description

The <b>CertGetIntendedKeyUsage</b> function acquires the intended key usage bytes from a certificate. The intended key usage can be in either the szOID_KEY_USAGE ("2.5.29.15") or szOID_KEY_ATTRIBUTES ("2.5.29.2") extension.

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertInfo [in]

A pointer to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure of the specified certificate.

### -param pbKeyUsage [out]

A pointer to a buffer to receive the intended key usage. The following list shows currently defined values. These can be combined by using bitwise-<b>OR</b> operations.

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>

### -param cbKeyUsage [in]

The size, in bytes, of the buffer pointed to by <i>pbKeyUsage</i>. Currently, the intended key usage occupies 1 or 2 bytes of data.

## -returns

If the certificate does not have any intended key usage bytes, <b>FALSE</b> is returned and <i>pbKeyUsage</i> is zeroed. Otherwise, <b>TRUE</b> is returned and up to <i>cbKeyUsage</i> number of bytes are copied into <i>pbKeyUsage</i>. Any remaining bytes not copied are zeroed.


<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns zero if none of the required extensions is found.

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>