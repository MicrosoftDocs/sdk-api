---
UID: NF:wincrypt.CertVerifyValidityNesting
title: CertVerifyValidityNesting function (wincrypt.h)
description: The CertVerifyValidityNesting function verifies that a subject certificate's time validity nests correctly within its issuer's time validity.
helpviewer_keywords: ["CertVerifyValidityNesting","CertVerifyValidityNesting function [Security]","_crypto2_certverifyvaliditynesting","security.certverifyvaliditynesting","wincrypt/CertVerifyValidityNesting"]
old-location: security\certverifyvaliditynesting.htm
tech.root: security
ms.assetid: dc73a21d-5b55-45c4-80d2-220508d9f762
ms.date: 12/05/2018
ms.keywords: CertVerifyValidityNesting, CertVerifyValidityNesting function [Security], _crypto2_certverifyvaliditynesting, security.certverifyvaliditynesting, wincrypt/CertVerifyValidityNesting
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
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertVerifyValidityNesting
 - wincrypt/CertVerifyValidityNesting
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
 - CertVerifyValidityNesting
---

# CertVerifyValidityNesting function


## -description

The <b>CertVerifyValidityNesting</b> function verifies that a subject certificate's time validity nests correctly within its issuer's time validity.

## -parameters

### -param pSubjectInfo [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure of the subject certificate.

### -param pIssuerInfo [in]

A pointer to the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure of the issuer certificate.

## -returns

Returns <b>TRUE</b> if the <b>NotBefore</b> time of the subject's certificate is after the <b>NotBefore</b> time of the issuer's certificate and the <b>NotAfter</b> time of the subject's certificate is not after the <b>NotAfter</b> time of the issuer's certificate. Otherwise, returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrlrevocation">CertVerifyCRLRevocation</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycrltimevalidity">CertVerifyCRLTimeValidity</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifytimevalidity">CertVerifyTimeValidity</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>