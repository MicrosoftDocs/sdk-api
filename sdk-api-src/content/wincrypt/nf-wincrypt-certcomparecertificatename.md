---
UID: NF:wincrypt.CertCompareCertificateName
title: CertCompareCertificateName function (wincrypt.h)
description: The CertCompareCertificateName function compares two certificate CERT_NAME_BLOB structures to determine whether they are identical. The CERT_NAME_BLOB structures are used for the subject and the issuer of certificates.
helpviewer_keywords: ["CertCompareCertificateName","CertCompareCertificateName function [Security]","_crypto2_certcomparecertificatename","security.certcomparecertificatename","wincrypt/CertCompareCertificateName"]
old-location: security\certcomparecertificatename.htm
tech.root: security
ms.assetid: 6249429d-0cb2-4209-9580-87185d44b967
ms.date: 12/05/2018
ms.keywords: CertCompareCertificateName, CertCompareCertificateName function [Security], _crypto2_certcomparecertificatename, security.certcomparecertificatename, wincrypt/CertCompareCertificateName
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
 - CertCompareCertificateName
 - wincrypt/CertCompareCertificateName
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
 - CertCompareCertificateName
---

# CertCompareCertificateName function


## -description

The <b>CertCompareCertificateName</b> function compares two certificate 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structures to determine whether they are identical. The <b>CERT_NAME_BLOB</b> structures are used for the subject and the issuer of certificates.

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pCertName1 [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> for the first name in the comparison. For more information, see 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>.

### -param pCertName2 [in]

A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> for the second name in the comparison.

## -returns

If the names are identical and the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcomparecertificate">CertCompareCertificate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>