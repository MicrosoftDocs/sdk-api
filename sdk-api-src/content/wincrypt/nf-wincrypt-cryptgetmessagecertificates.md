---
UID: NF:wincrypt.CryptGetMessageCertificates
title: CryptGetMessageCertificates function (wincrypt.h)
description: The CryptGetMessageCertificates function returns the handle of an open certificate store containing the message's certificates and CRLs. This function calls CertOpenStore using provider type CERT_STORE_PROV_PKCS7 as its lpszStoreProvider parameter.
helpviewer_keywords: ["CryptGetMessageCertificates","CryptGetMessageCertificates function [Security]","_crypto2_cryptgetmessagecertificates","security.cryptgetmessagecertificates","wincrypt/CryptGetMessageCertificates"]
old-location: security\cryptgetmessagecertificates.htm
tech.root: security
ms.assetid: d890f91f-bb45-463b-b7c0-56acc9367571
ms.date: 12/05/2018
ms.keywords: CryptGetMessageCertificates, CryptGetMessageCertificates function [Security], _crypto2_cryptgetmessagecertificates, security.cryptgetmessagecertificates, wincrypt/CryptGetMessageCertificates
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
 - CryptGetMessageCertificates
 - wincrypt/CryptGetMessageCertificates
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
 - CryptGetMessageCertificates
---

# CryptGetMessageCertificates function


## -description

The <b>CryptGetMessageCertificates</b> function returns the handle of an open <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> containing the message's certificates and <a href="/windows/desktop/SecGloss/c-gly">CRLs</a>. This function calls 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> using provider type CERT_STORE_PROV_PKCS7 as its <i>lpszStoreProvider</i> parameter.

## -parameters

### -param dwMsgAndCertEncodingType [in]

Specifies the encoding type used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param hCryptProv [in]

This parameter is not used and should be set to <b>NULL</b>.

<b>Windows Server 2003 and Windows XP:  </b>Handle of the CSP passed to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>.Unless there is a strong reason for passing a specific cryptographic provider in <i>hCryptProv</i>, pass zero to cause the default RSA or DSS provider to be acquired.

This parameter's data type is <b>HCRYPTPROV</b>.

### -param dwFlags [in]

Flags passed to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>.

### -param pbSignedBlob [in]

A pointer to a buffered 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the signed message.

### -param cbSignedBlob [in]

The size, in bytes, of the signed message.

## -returns

Returns the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> containing the message's certificates and CRLs. For an error, <b>NULL</b> is returned.

The following lists the error code most commonly returned by the 
		       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid message and certificate encoding types. Currently only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING are supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

Use 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine the reason for any errors.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-setting-and-getting-certificate-store-properties">Example C Program: Setting and Getting Certificate Store Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Simplified Message Functions</a>