---
UID: NF:wincrypt.CertCreateCertificateContext
title: CertCreateCertificateContext function (wincrypt.h)
description: Creates a certificate context from an encoded certificate. The created context is not persisted to a certificate store. The function makes a copy of the encoded certificate within the created context.
helpviewer_keywords: ["CertCreateCertificateContext","CertCreateCertificateContext function [Security]","_crypto2_certcreatecertificatecontext","security.certcreatecertificatecontext","wincrypt/CertCreateCertificateContext"]
old-location: security\certcreatecertificatecontext.htm
tech.root: security
ms.assetid: a32714c4-ee88-48a8-a40a-bbbfec0613ac
ms.date: 12/05/2018
ms.keywords: CertCreateCertificateContext, CertCreateCertificateContext function [Security], _crypto2_certcreatecertificatecontext, security.certcreatecertificatecontext, wincrypt/CertCreateCertificateContext
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
 - CertCreateCertificateContext
 - wincrypt/CertCreateCertificateContext
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
 - CertCreateCertificateContext
---

# CertCreateCertificateContext function


## -description

The <b>CertCreateCertificateContext</b> function creates a certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> from an encoded certificate. The created context is not persisted to a certificate store. The function makes a copy of the encoded certificate within the created context.

## -parameters

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCertEncoded [in]

A pointer to a buffer that contains the encoded certificate from which the context is to be created.

### -param cbCertEncoded [in]

The size, in bytes, of the <i>pbCertEncoded</i> buffer.

## -returns

If the function succeeds, the function returns a pointer to a read-only 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. When you have finished using the certificate context, free it by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

If the function is unable to decode and create the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>, it returns <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

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
A certificate encoding type that is not valid was specified. Currently, only the X509_ASN_ENCODING type is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

The 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> must be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> can be called to make a duplicate. 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> can be called to store and read properties for the certificate.


#### Examples

The following example shows creating a certificate context from an encoded certificate. The created context is not put in a certificate store. For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-certificate-store-operations">Example C Program: Certificate Store Operations</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void main()
{
	PCCERT_CONTEXT  pCertContext = NULL; 

	//------------------------------------------------------------------ 
	//  Create a new certificate from the encoded part of
	//  an available certificate. pDesiredCert is a previously
	//  assigned PCCERT_CONTEXT variable.
	if(pCertContext = CertCreateCertificateContext(
		MY_ENCODING_TYPE,              // The encoding type
		pDesiredCert->pbCertEncoded,   // The encoded data from
									   // the certificate retrieved
		pDesiredCert->cbCertEncoded))  // The length of the encoded data
	{
		printf("A new certificate has been created.\n");
	 
		// Use the certificate context as needed.
		// ...

		// When finished, free the certificate context.
		CertFreeCertificateContext(pCertContext);
	}
	else
	{
		printf("A new certificate could not be created.\n");
		exit(1);
	}
}
```

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecrlcontext">CertCreateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatectlcontext">CertCreateCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>