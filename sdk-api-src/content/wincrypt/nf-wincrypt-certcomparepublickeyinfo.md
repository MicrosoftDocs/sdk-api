---
UID: NF:wincrypt.CertComparePublicKeyInfo
title: CertComparePublicKeyInfo function (wincrypt.h)
description: The CertComparePublicKeyInfo function compares two encoded public keys to determine whether they are identical.
helpviewer_keywords: ["CertComparePublicKeyInfo","CertComparePublicKeyInfo function [Security]","_crypto2_certcomparepublickeyinfo","security.certcomparepublickeyinfo","wincrypt/CertComparePublicKeyInfo"]
old-location: security\certcomparepublickeyinfo.htm
tech.root: security
ms.assetid: 079e4d5e-c8cb-4c3e-8094-13b9a140d564
ms.date: 12/05/2018
ms.keywords: CertComparePublicKeyInfo, CertComparePublicKeyInfo function [Security], _crypto2_certcomparepublickeyinfo, security.certcomparepublickeyinfo, wincrypt/CertComparePublicKeyInfo
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertComparePublicKeyInfo
 - wincrypt/CertComparePublicKeyInfo
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
 - CertComparePublicKeyInfo
---

# CertComparePublicKeyInfo function


## -description

The <b>CertComparePublicKeyInfo</b> function compares two encoded public keys to determine whether they are identical.

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pPublicKey1 [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> for the first public key in the comparison.

### -param pPublicKey2 [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> for the second public key in the comparison.

## -returns

If the public keys are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>