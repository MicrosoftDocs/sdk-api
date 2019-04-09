---
UID: NF:wincrypt.CertCreateCertificateContext
title: CertCreateCertificateContext function (wincrypt.h)
author: windows-sdk-content
description: Creates a certificate context from an encoded certificate. The created context is not persisted to a certificate store. The function makes a copy of the encoded certificate within the created context.
old-location: security\certcreatecertificatecontext.htm
tech.root: SecCrypto
ms.assetid: a32714c4-ee88-48a8-a40a-bbbfec0613ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertCreateCertificateContext, CertCreateCertificateContext function [Security], _crypto2_certcreatecertificatecontext, security.certcreatecertificatecontext, wincrypt/CertCreateCertificateContext
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertCreateCertificateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertCreateCertificateContext function


## -description


The <b>CertCreateCertificateContext</b> function creates a certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> from an encoded certificate. The created context is not persisted to a certificate store. The function makes a copy of the encoded certificate within the created context.


## -parameters




### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

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
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>. When you have finished using the certificate context, free it by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.

If the function is unable to decode and create the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>, it returns <b>NULL</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Some possible error codes follow.

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
 

If the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> may return an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="https://msdn.microsoft.com/cb1f34dd-dab4-4ffb-a73b-79a214290509">ASN.1 Encoding/Decoding Return Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> must be freed by calling 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. 
<a href="https://msdn.microsoft.com/589edd25-c8d0-4f93-83b2-9df2ed2e2812">CertDuplicateCertificateContext</a> can be called to make a duplicate. 
<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a> and 
<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a> can be called to store and read properties for the certificate.


#### Examples

The following example shows creating a certificate context from an encoded certificate. The created context is not put in a certificate store. For another example that uses this function, see <a href="https://msdn.microsoft.com/cf87791c-b98c-4dd7-b346-336c4b1a88ca">Example C Program: Certificate Store Operations</a>.


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




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/23d9dfb0-926d-443e-b960-a03338f1cc1b">CertCreateCRLContext</a>



<a href="https://msdn.microsoft.com/172c59ee-9e06-4169-aaa7-2624e3fcf015">CertCreateCTLContext</a>



<a href="https://msdn.microsoft.com/589edd25-c8d0-4f93-83b2-9df2ed2e2812">CertDuplicateCertificateContext</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="https://msdn.microsoft.com/f766db64-3121-4f70-ac83-ce25ee634efa">CertGetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/b4a0c66d-997f-49cb-935a-9187320037f1">CertSetCertificateContextProperty</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Functions</a>
 

 

