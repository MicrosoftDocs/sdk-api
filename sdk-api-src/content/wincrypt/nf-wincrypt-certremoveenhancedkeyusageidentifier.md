---
UID: NF:wincrypt.CertRemoveEnhancedKeyUsageIdentifier
title: CertRemoveEnhancedKeyUsageIdentifier function (wincrypt.h)
description: The CertRemoveEnhancedKeyUsageIdentifier function removes a usage identifier object identifier (OID) from the enhanced key usage (EKU) extended property of the certificate.
helpviewer_keywords: ["CertRemoveEnhancedKeyUsageIdentifier","CertRemoveEnhancedKeyUsageIdentifier function [Security]","_crypto2_certremoveenhancedkeyusageidentifier","security.certremoveenhancedkeyusageidentifier","wincrypt/CertRemoveEnhancedKeyUsageIdentifier"]
old-location: security\certremoveenhancedkeyusageidentifier.htm
tech.root: security
ms.assetid: 4fb27073-674c-4bac-9a62-6e33e1a5785e
ms.date: 12/05/2018
ms.keywords: CertRemoveEnhancedKeyUsageIdentifier, CertRemoveEnhancedKeyUsageIdentifier function [Security], _crypto2_certremoveenhancedkeyusageidentifier, security.certremoveenhancedkeyusageidentifier, wincrypt/CertRemoveEnhancedKeyUsageIdentifier
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
 - CertRemoveEnhancedKeyUsageIdentifier
 - wincrypt/CertRemoveEnhancedKeyUsageIdentifier
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
 - CertRemoveEnhancedKeyUsageIdentifier
---

# CertRemoveEnhancedKeyUsageIdentifier function


## -description

The <b>CertRemoveEnhancedKeyUsageIdentifier</b> function removes a usage identifier <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) from the <a href="/windows/desktop/SecGloss/e-gly">enhanced key usage</a> (EKU) extended property of the certificate.

## -parameters

### -param pCertContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the certificate for which the usage identifier OID is to be removed.

### -param pszUsageIdentifier [in]

A pointer to the usage identifier OID to remove.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Enhanced Key Usage Functions</a>