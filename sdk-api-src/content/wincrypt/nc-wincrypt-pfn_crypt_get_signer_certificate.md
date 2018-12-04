---
UID: NC:wincrypt.PFN_CRYPT_GET_SIGNER_CERTIFICATE
title: PFN_CRYPT_GET_SIGNER_CERTIFICATE
author: windows-sdk-content
description: The CryptGetSignerCertificateCallback user supplied callback function is used with the CRYPT_VERIFY_MESSAGE_PARA structure to get and verify a message signer's certificate.
old-location: security\cryptgetsignercertificatecallback.htm
tech.root: seccrypto
ms.assetid: 557ebb26-cce0-4c41-b49c-769b2831cf35
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CryptGetSignerCertificateCallback, CryptGetSignerCertificateCallback callback function [Security], PFN_CRYPT_GET_SIGNER_CERTIFICATE, PFN_CRYPT_GET_SIGNER_CERTIFICATE callback, security.cryptgetsignercertificatecallback, wincrypt/CryptGetSignerCertificateCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CryptGetSignerCertificateCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CRYPT_GET_SIGNER_CERTIFICATE callback function


## -description


The <b>CryptGetSignerCertificateCallback</b> user supplied callback function is used with the <a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure to get and verify a message signer's certificate.


## -parameters




### -param *pvGetArg [in]

A pointer to user-defined data passed on to the verification function as specified in the <a href="https://msdn.microsoft.com/bbd56b5e-2bbe-420f-8842-1be50dca779f">CRYPT_VERIFY_MESSAGE_PARA</a> structure.


### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pSignerId [in]

A pointer to a <a href="https://msdn.microsoft.com/8d0a3053-52d4-437a-bf55-6724b5825cdc">CERT_INFO</a> structure containing the issuer and serial number. Can be <b>NULL</b> if there is no content or signer.


### -param hMsgCertStore [in]

A handle to the certificate store containing all the certificates and CRLs in the signed message.


## -returns



If a signer certificate is found, the function returns a pointer to a read-only <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>. The returned <b>CERT_CONTEXT</b> was obtained either from a certificate store or was created using <a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a>. In either case, it must be freed using <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>. If this function fails, the return value is <b>NULL</b>.




## -remarks



If the message does not contain content or signers, the function is called with <i>pSignerId</i> set to <b>NULL</b>.



