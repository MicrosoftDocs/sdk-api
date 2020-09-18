---
UID: NF:wincrypt.CertFindCertificateInCRL
title: CertFindCertificateInCRL function (wincrypt.h)
description: The CertFindCertificateInCRL function searches the certificate revocation list (CRL) for the specified certificate.
helpviewer_keywords: ["CertFindCertificateInCRL","CertFindCertificateInCRL function [Security]","_crypto2_certfindcertificateincrl","security.certfindcertificateincrl","wincrypt/CertFindCertificateInCRL"]
old-location: security\certfindcertificateincrl.htm
tech.root: security
ms.assetid: c05a99e6-da38-431e-8d02-04056047a211
ms.date: 12/05/2018
ms.keywords: CertFindCertificateInCRL, CertFindCertificateInCRL function [Security], _crypto2_certfindcertificateincrl, security.certfindcertificateincrl, wincrypt/CertFindCertificateInCRL
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
 - CertFindCertificateInCRL
 - wincrypt/CertFindCertificateInCRL
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
 - CertFindCertificateInCRL
---

# CertFindCertificateInCRL function


## -description

The <b>CertFindCertificateInCRL</b> function searches the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) for the specified certificate.

## -parameters

### -param pCert [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the certificate to be searched for in the CRL.

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> to be searched.

### -param dwFlags [in]

Reserved for future use. Must be set to zero.

### -param pvReserved [in, optional]

Reserved for future use. Must be set to zero.

### -param ppCrlEntry [out]

If the certificate is found in the CRL, this pointer is updated with a pointer to the entry. Otherwise, it is set to <b>NULL</b>. The returned entry is not allocated and must not be freed.

## -returns

<b>TRUE</b> if the list was searched; otherwise <b>FALSE</b>.