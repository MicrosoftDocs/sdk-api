---
UID: NS:wincrypt._CERT_CONTEXT
title: CERT_CONTEXT
author: windows-sdk-content
description: Contains both the encoded and decoded representations of a certificate.
old-location: security\cert_context.htm
tech.root: seccrypto
ms.assetid: f0a3200e-6541-423d-a4a3-595a31026eea
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCERT_CONTEXT, CERT_CONTEXT, CERT_CONTEXT structure [Security], PCCERT_CONTEXT, PCCERT_CONTEXT structure pointer [Security], PCERT_CONTEXT, PCERT_CONTEXT structure pointer [Security], _crypto2_cert_context, security.cert_context, wincrypt/CERT_CONTEXT, wincrypt/PCCERT_CONTEXT, wincrypt/PCERT_CONTEXT"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_CONTEXT
product: Windows
targetos: Windows
req.typenames: CERT_CONTEXT, *PCERT_CONTEXT
req.redist: 
---

# CERT_CONTEXT structure


## -description


The <b>CERT_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>. A certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> returned by one of the functions defined in Wincrypt.h must be freed by calling the 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function. The 
<a href="https://msdn.microsoft.com/589edd25-c8d0-4f93-83b2-9df2ed2e2812">CertDuplicateCertificateContext</a> function can be called to make a duplicate copy (which also must be freed by calling <b>CertFreeCertificateContext</b>).


## -struct-fields




### -field dwCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>



### -field pbCertEncoded

A pointer to a buffer that contains the encoded certificate.


### -field cbCertEncoded

The size, in bytes, of the encoded certificate.


### -field pCertInfo

The address of a <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure that contains the certificate information.


### -field hCertStore

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> that contains the certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.


## -see-also




<a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a>



<a href="https://msdn.microsoft.com/1601d860-6054-4650-a033-ea088655b7e4">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a>



<a href="https://msdn.microsoft.com/5e4d8cae-1096-491f-9a04-92b7e9c020bb">CertAddCertificateContextToStore</a>



<a href="https://msdn.microsoft.com/7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d">CertAddEncodedCertificateToStore</a>



<a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a>



<a href="https://msdn.microsoft.com/c5ab5b4c-dc0c-416b-aa9e-b939398cfa6d">CertEnumCertificatesInStore</a>



<a href="https://msdn.microsoft.com/20b3fcfb-55df-46ff-80a5-70f31a3d03b2">CertFindCertificateInStore</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="https://msdn.microsoft.com/b57982d0-cba8-43cd-a544-3635fdf599e2">CertGetIssuerCertificateFromStore</a>



<a href="https://msdn.microsoft.com/61d73501-91b1-4498-b1a3-17392360c700">CertGetSubjectCertificateFromStore</a>



<a href="https://msdn.microsoft.com/2d6fb244-5273-4530-bec4-e5451fe26f2e">CertVerifyRevocation</a>



<a href="https://msdn.microsoft.com/03411e7a-b097-4059-a198-3d412ae40e38">CryptVerifyMessageSignature</a>
 

 

