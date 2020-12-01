---
UID: NF:wincrypt.CertCreateCRLContext
title: CertCreateCRLContext function (wincrypt.h)
description: The CertCreateCRLContext function creates a certificate revocation list (CRL) context from an encoded CRL. The created context is not persisted to a certificate store. It makes a copy of the encoded CRL within the created context.
helpviewer_keywords: ["CertCreateCRLContext","CertCreateCRLContext function [Security]","_crypto2_certcreatecrlcontext","security.certcreatecrlcontext","wincrypt/CertCreateCRLContext"]
old-location: security\certcreatecrlcontext.htm
tech.root: security
ms.assetid: 23d9dfb0-926d-443e-b960-a03338f1cc1b
ms.date: 12/05/2018
ms.keywords: CertCreateCRLContext, CertCreateCRLContext function [Security], _crypto2_certcreatecrlcontext, security.certcreatecrlcontext, wincrypt/CertCreateCRLContext
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
 - CertCreateCRLContext
 - wincrypt/CertCreateCRLContext
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
 - CertCreateCRLContext
---

# CertCreateCRLContext function


## -description

The <b>CertCreateCRLContext</b> function creates a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) <a href="/windows/desktop/SecGloss/c-gly">context</a> from an encoded CRL. The created context is not persisted to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. It makes a copy of the encoded CRL within the created context.

## -parameters

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCrlEncoded [in]

A pointer to a buffer containing the encoded <a href="/windows/desktop/SecGloss/c-gly">CRL</a> from which the context is to be created.

### -param cbCrlEncoded [in]

The size, in bytes, of the <i>pbCrlEncoded</i> buffer.

## -returns

If the function succeeds, the return value is a pointer to a read-only 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>.

If the function fails and is unable to decode and create the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>, the return value is <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table shows a possible error code.

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
Invalid certificate encoding type. Currently, only the encoding type X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a> can be called to make a duplicate. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a> can be called to store and read properties for the CRL.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatectlcontext">CertCreateCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>