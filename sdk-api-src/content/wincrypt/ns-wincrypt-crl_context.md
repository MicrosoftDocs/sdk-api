---
UID: NS:wincrypt._CRL_CONTEXT
title: CRL_CONTEXT (wincrypt.h)
description: The CRL_CONTEXT structure contains both the encoded and decoded representations of a certificate revocation list (CRL). CRL contexts returned by any CryptoAPI function must be freed by calling the CertFreeCRLContext function.
helpviewer_keywords: ["*PCRL_CONTEXT","CRL_CONTEXT","CRL_CONTEXT structure [Security]","PCCRL_CONTEXT","PCCRL_CONTEXT structure pointer [Security]","PCRL_CONTEXT","PCRL_CONTEXT structure pointer [Security]","_crypto2_crl_context","security.crl_context","wincrypt/CRL_CONTEXT","wincrypt/PCCRL_CONTEXT","wincrypt/PCRL_CONTEXT"]
old-location: security\crl_context.htm
tech.root: security
ms.assetid: cf7cabcd-b469-492a-b855-8870465ea1cc
ms.date: 12/05/2018
ms.keywords: '*PCRL_CONTEXT, CRL_CONTEXT, CRL_CONTEXT structure [Security], PCCRL_CONTEXT, PCCRL_CONTEXT structure pointer [Security], PCRL_CONTEXT, PCRL_CONTEXT structure pointer [Security], _crypto2_crl_context, security.crl_context, wincrypt/CRL_CONTEXT, wincrypt/PCCRL_CONTEXT, wincrypt/PCRL_CONTEXT'
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
req.typenames: CRL_CONTEXT, *PCRL_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRL_CONTEXT
 - wincrypt/_CRL_CONTEXT
 - PCRL_CONTEXT
 - wincrypt/PCRL_CONTEXT
 - CRL_CONTEXT
 - wincrypt/CRL_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CRL_CONTEXT
---

# CRL_CONTEXT structure


## -description

The <b>CRL_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL). CRL contexts returned by any CryptoAPI function must be freed by calling the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> function.

## -struct-fields

### -field dwCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field pbCrlEncoded

A pointer to the encoded CRL information.

### -field cbCrlEncoded

The size, in bytes, of the encoded CRL information.

### -field pCrlInfo

A pointer to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a> structure containing the CRL information.

### -field hCertStore

A handle to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_sign_message_para">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecrlcontext">CertCreateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlfromstore">CertGetCRLFromStore</a>