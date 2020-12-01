---
UID: NF:wincrypt.CertCompareCertificate
title: CertCompareCertificate function (wincrypt.h)
description: Determines whether two certificates are identical by comparing the issuer name and serial number of the certificates.
helpviewer_keywords: ["CertCompareCertificate","CertCompareCertificate function [Security]","_crypto2_certcomparecertificate","security.certcomparecertificate","wincrypt/CertCompareCertificate"]
old-location: security\certcomparecertificate.htm
tech.root: security
ms.assetid: b485fa81-b927-4f0c-bde1-075f36c76d9a
ms.date: 12/05/2018
ms.keywords: CertCompareCertificate, CertCompareCertificate function [Security], _crypto2_certcomparecertificate, security.certcomparecertificate, wincrypt/CertCompareCertificate
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
 - CertCompareCertificate
 - wincrypt/CertCompareCertificate
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
 - CertCompareCertificate
---

# CertCompareCertificate function


## -description

The <b>CertCompareCertificate</b> function determines whether two certificates are identical by comparing the issuer name and serial number of the certificates.
<div class="alert"><b>Caution</b>  The <b>CertCompareCertificate</b> function must not be used for security assertions because it does not compare <a href="/windows/desktop/SecGloss/b-gly">BLOBs</a>.</div><div> </div>

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertId1 [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> for the first certificate in the comparison.

### -param pCertId2 [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> for the second certificate in the comparison.

## -returns

If the certificates are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcomparecertificatename">CertCompareCertificateName</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>