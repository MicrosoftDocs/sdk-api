---
UID: NS:wincrypt._CERT_CONTEXT
title: CERT_CONTEXT (wincrypt.h)
description: Contains both the encoded and decoded representations of a certificate.
helpviewer_keywords: ["*PCERT_CONTEXT","CERT_CONTEXT","CERT_CONTEXT structure [Security]","PCCERT_CONTEXT","PCCERT_CONTEXT structure pointer [Security]","PCERT_CONTEXT","PCERT_CONTEXT structure pointer [Security]","_crypto2_cert_context","security.cert_context","wincrypt/CERT_CONTEXT","wincrypt/PCCERT_CONTEXT","wincrypt/PCERT_CONTEXT"]
old-location: security\cert_context.htm
tech.root: security
ms.assetid: f0a3200e-6541-423d-a4a3-595a31026eea
ms.date: 12/05/2018
ms.keywords: '*PCERT_CONTEXT, CERT_CONTEXT, CERT_CONTEXT structure [Security], PCCERT_CONTEXT, PCCERT_CONTEXT structure pointer [Security], PCERT_CONTEXT, PCERT_CONTEXT structure pointer [Security], _crypto2_cert_context, security.cert_context, wincrypt/CERT_CONTEXT, wincrypt/PCCERT_CONTEXT, wincrypt/PCERT_CONTEXT'
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
req.typenames: CERT_CONTEXT, *PCERT_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CONTEXT
 - wincrypt/_CERT_CONTEXT
 - PCERT_CONTEXT
 - wincrypt/PCERT_CONTEXT
 - CERT_CONTEXT
 - wincrypt/CERT_CONTEXT
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
 - CERT_CONTEXT
---

# CERT_CONTEXT structure


## -description

The <b>CERT_CONTEXT</b> structure contains both the encoded and decoded representations of a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. A certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> returned by one of the functions defined in Wincrypt.h must be freed by calling the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function. The 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> function can be called to make a duplicate copy (which also must be freed by calling <b>CertFreeCertificateContext</b>).

## -struct-fields

### -field dwCertEncodingType

Type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

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

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure that contains the certificate information.

### -field hCertStore

A handle to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that contains the certificate <a href="/windows/desktop/SecGloss/c-gly">context</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_sign_message_para">CRYPT_SIGN_MESSAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_verify_message_para">CRYPT_VERIFY_MESSAGE_PARA</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore">CertAddCertificateContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumcertificatesinstore">CertEnumCertificatesInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetissuercertificatefromstore">CertGetIssuerCertificateFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore">CertGetSubjectCertificateFromStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyrevocation">CertVerifyRevocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifymessagesignature">CryptVerifyMessageSignature</a>