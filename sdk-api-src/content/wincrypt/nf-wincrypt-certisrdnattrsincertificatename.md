---
UID: NF:wincrypt.CertIsRDNAttrsInCertificateName
title: CertIsRDNAttrsInCertificateName function (wincrypt.h)
description: The CertIsRDNAttrsInCertificateName function compares the attributes in the certificate name with the specified CERT_RDN to determine whether all attributes are included there.
helpviewer_keywords: ["CertIsRDNAttrsInCertificateName","CertIsRDNAttrsInCertificateName function [Security]","_crypto2_certisrdnattrsincertificatename","security.certisrdnattrsincertificatename","wincrypt/CertIsRDNAttrsInCertificateName"]
old-location: security\certisrdnattrsincertificatename.htm
tech.root: security
ms.assetid: e45b80a3-9269-4f21-8407-1c8303cb5f32
ms.date: 12/05/2018
ms.keywords: CertIsRDNAttrsInCertificateName, CertIsRDNAttrsInCertificateName function [Security], _crypto2_certisrdnattrsincertificatename, security.certisrdnattrsincertificatename, wincrypt/CertIsRDNAttrsInCertificateName
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
 - CertIsRDNAttrsInCertificateName
 - wincrypt/CertIsRDNAttrsInCertificateName
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
 - CertIsRDNAttrsInCertificateName
---

# CertIsRDNAttrsInCertificateName function


## -description

The <b>CertIsRDNAttrsInCertificateName</b> function compares the attributes in the <a href="/windows/desktop/SecGloss/c-gly">certificate name</a> with the specified 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> to determine whether all attributes are included there. The comparison iterates through the <b>CERT_RDN</b> and looks for an attribute match in any of the <b>CERT_RDN</b>s of the certificate name.

## -parameters

### -param dwCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param dwFlags [in]

CERT_UNICODE_IS_RDN_ATTRS_FLAG must be set if the <i>pRDN</i> was initialized with Unicode strings as in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> with <i>lpszStructType</i> set to X509_UNICODE_NAME.

CERT_CASE_INSENSITIVE_IS_RDN_ATTRS_FLAG is set to do a case insensitive match. Otherwise, an exact, case sensitive match is done.

### -param pCertName [in]

A pointer to a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> that contains the encoded subject or issuer name.

### -param pRDN [in]

Array of 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structures that contain the attributes to be found in the name. The 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> member of the <b>CERT_RDN</b> structure behaves according to the following rules.

<ul>
<li>If <b>pszObjId</b> is <b>NULL</b>, the attribute <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) is ignored.</li>
<li>If <b>dwValueType</b> is CERT_RDN_ANY_TYPE, the value type is ignored.</li>
<li>If the <b>pbData</b> member of <b>Value</b> is  <b>NULL</b>, any value can be a match.</li>
</ul>

## -returns

If the function succeeds and all of the RDN values in the specified <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> are in the certificate name, the return value is nonzero (<b>TRUE</b>).

If the function fails, or if there are  RDN values in the specified <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> that are not in the certificate name, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following table lists some possible error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NO_MATCH</b></dt>
</dl>
</td>
<td width="60%">
Not all the attributes were found and matched.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Invalid certificate encoding type. Currently only X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

Currently, only an exact, case-sensitive match is supported.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>