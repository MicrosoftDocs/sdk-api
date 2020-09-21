---
UID: NF:wincrypt.CertCreateCTLContext
title: CertCreateCTLContext function (wincrypt.h)
description: The CertCreateCTLContext function creates a certificate trust list (CTL) context from an encoded CTL. The created context is not persisted to a certificate store. The function makes a copy of the encoded CTL within the created context.
helpviewer_keywords: ["CertCreateCTLContext","CertCreateCTLContext function [Security]","_crypto2_certcreatectlcontext","security.certcreatectlcontext","wincrypt/CertCreateCTLContext"]
old-location: security\certcreatectlcontext.htm
tech.root: security
ms.assetid: 172c59ee-9e06-4169-aaa7-2624e3fcf015
ms.date: 12/05/2018
ms.keywords: CertCreateCTLContext, CertCreateCTLContext function [Security], _crypto2_certcreatectlcontext, security.certcreatectlcontext, wincrypt/CertCreateCTLContext
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
 - CertCreateCTLContext
 - wincrypt/CertCreateCTLContext
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
 - CertCreateCTLContext
---

# CertCreateCTLContext function


## -description

The <b>CertCreateCTLContext</b> function creates a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context from an encoded CTL. The created context is not persisted to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. The function makes a copy of the encoded CTL within the created context.

## -parameters

### -param dwMsgAndCertEncodingType [in]

Specifies the type of encoding used. Both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> must be specified by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCtlEncoded [in]

A pointer to a buffer containing the encoded CTL from which the context is to be created.

### -param cbCtlEncoded [in]

The size, in bytes, of the <i>pbCtlEncoded</i> buffer.

## -returns

If the function succeeds, the return value is a pointer to a read-only 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>.

If the function fails and is unable to decode and create the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>, the return value is <b>NULL</b>. For extended error information, call 
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
Invalid certificate encoding type. Only PKCS_7_ASN_ENCODING and X509_ASN_ENCODING are supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a> can be called to make a duplicate. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetctlcontextproperty">CertSetCTLContextProperty</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a> can be called to store and read properties for the CTL.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecrlcontext">CertCreateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetctlcontextproperty">CertSetCTLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>