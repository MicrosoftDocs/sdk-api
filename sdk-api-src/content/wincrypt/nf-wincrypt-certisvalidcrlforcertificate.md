---
UID: NF:wincrypt.CertIsValidCRLForCertificate
title: CertIsValidCRLForCertificate function (wincrypt.h)
description: The CertIsValidCRLForCertificate function checks a CRL to find out if it is a CRL that would include a specific certificate if that certificate were revoked.
helpviewer_keywords: ["CertIsValidCRLForCertificate","CertIsValidCRLForCertificate function [Security]","_crypto2_certisvalidcrlforcertificate","security.certisvalidcrlforcertificate","wincrypt/CertIsValidCRLForCertificate"]
old-location: security\certisvalidcrlforcertificate.htm
tech.root: security
ms.assetid: 06047b7a-4bdd-42f9-bb85-49b6ec6f35a0
ms.date: 12/05/2018
ms.keywords: CertIsValidCRLForCertificate, CertIsValidCRLForCertificate function [Security], _crypto2_certisvalidcrlforcertificate, security.certisvalidcrlforcertificate, wincrypt/CertIsValidCRLForCertificate
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
 - CertIsValidCRLForCertificate
 - wincrypt/CertIsValidCRLForCertificate
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
 - CertIsValidCRLForCertificate
---

# CertIsValidCRLForCertificate function


## -description

The <b>CertIsValidCRLForCertificate</b> function checks a <a href="/windows/desktop/SecGloss/c-gly">CRL</a> to find out if it is a CRL that would include a specific certificate if that certificate were revoked. If the CRL has an issuing distribution point (IDP) extension, the function checks whether that IDP is valid for the certificate being checked.

## -parameters

### -param pCert [in]

A pointer to a certificate <a href="/windows/desktop/SecGloss/c-gly">context</a>.

### -param pCrl [in]

A pointer to a CRL. The function checks this CRL to determine whether it could contain the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> pointed to by <i>pCert</i>. The function does not look for the certificate in the CRL.

### -param dwFlags [in]

Currently not used and must be set to zero.

### -param pvReserved [in]

Currently not used and must be set to <b>NULL</b>.

## -returns

The function returns <b>TRUE</b> if the CRL is a valid CRL to be searched for the specific certificate. It returns <b>FALSE</b> if the CRL is not a valid CRL for searching for the certificate.

## -remarks

For the CRL to be valid for the certificate, the <b>CertIsValidCRLForCertificate</b> function does not require the CRL to be issued by the same <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) as the issuer of the certificate.