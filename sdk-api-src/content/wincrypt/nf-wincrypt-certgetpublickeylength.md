---
UID: NF:wincrypt.CertGetPublicKeyLength
title: CertGetPublicKeyLength function (wincrypt.h)
description: The CertGetPublicKeyLength function acquires the bit length of public/private keys from a public key BLOB.
helpviewer_keywords: ["CertGetPublicKeyLength","CertGetPublicKeyLength function [Security]","_crypto2_certgetpublickeylength","security.certgetpublickeylength","wincrypt/CertGetPublicKeyLength"]
old-location: security\certgetpublickeylength.htm
tech.root: security
ms.assetid: e67923f4-cd1f-4952-88f1-92ee26423f87
ms.date: 12/05/2018
ms.keywords: CertGetPublicKeyLength, CertGetPublicKeyLength function [Security], _crypto2_certgetpublickeylength, security.certgetpublickeylength, wincrypt/CertGetPublicKeyLength
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
 - CertGetPublicKeyLength
 - wincrypt/CertGetPublicKeyLength
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
 - CertGetPublicKeyLength
---

# CertGetPublicKeyLength function


## -description

The <b>CertGetPublicKeyLength</b> function acquires the bit length of public/private keys from a <a href="/windows/desktop/SecGloss/p-gly">public key BLOB</a>.

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pPublicKey [in]

A pointer to the <a href="/windows/desktop/SecGloss/p-gly">public key BLOB</a> containing the keys for which the length is being retrieved.

## -returns

Returns the length of the public/private keys in bits. If unable to determine the key's length, returns zero.

Call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to see the reason for any failures.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>