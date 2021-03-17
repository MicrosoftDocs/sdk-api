---
UID: NC:wincrypt.PFN_CRYPT_GET_SIGNER_CERTIFICATE
title: PFN_CRYPT_GET_SIGNER_CERTIFICATE (wincrypt.h)
description: The CryptGetSignerCertificateCallback user supplied callback function is used with the CRYPT_VERIFY_MESSAGE_PARA structure to get and verify a message signer's certificate.
helpviewer_keywords: ["CryptGetSignerCertificateCallback","CryptGetSignerCertificateCallback callback function [Security]","PFN_CRYPT_GET_SIGNER_CERTIFICATE","PFN_CRYPT_GET_SIGNER_CERTIFICATE callback","security.cryptgetsignercertificatecallback","wincrypt/CryptGetSignerCertificateCallback"]
old-location: security\cryptgetsignercertificatecallback.htm
tech.root: security
ms.assetid: 557ebb26-cce0-4c41-b49c-769b2831cf35
ms.date: 12/05/2018
ms.keywords: CryptGetSignerCertificateCallback, CryptGetSignerCertificateCallback callback function [Security], PFN_CRYPT_GET_SIGNER_CERTIFICATE, PFN_CRYPT_GET_SIGNER_CERTIFICATE callback, security.cryptgetsignercertificatecallback, wincrypt/CryptGetSignerCertificateCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CRYPT_GET_SIGNER_CERTIFICATE
 - wincrypt/PFN_CRYPT_GET_SIGNER_CERTIFICATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - CryptGetSignerCertificateCallback
---

# PFN_CRYPT_GET_SIGNER_CERTIFICATE callback function


## -description

The <b>CryptGetSignerCertificateCallback</b> user supplied callback function is used with the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure to get and verify a message signer's certificate.

## -parameters

### -param pvGetArg [in]

A pointer to user-defined data passed on to the verification function as specified in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a> structure.

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pSignerId [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure containing the issuer and serial number. Can be <b>NULL</b> if there is no content or signer.

### -param hMsgCertStore [in]

A handle to the certificate store containing all the certificates and CRLs in the signed message.

## -returns

If a signer certificate is found, the function returns a pointer to a read-only <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. The returned <b>CERT_CONTEXT</b> was obtained either from a certificate store or was created using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>. In either case, it must be freed using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. If this function fails, the return value is <b>NULL</b>.

## -remarks

If the message does not contain content or signers, the function is called with <i>pSignerId</i> set to <b>NULL</b>.
