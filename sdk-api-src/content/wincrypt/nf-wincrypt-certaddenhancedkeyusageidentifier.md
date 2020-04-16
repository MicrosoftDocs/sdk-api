---
UID: NF:wincrypt.CertAddEnhancedKeyUsageIdentifier
title: CertAddEnhancedKeyUsageIdentifier function (wincrypt.h)
description: The CertAddEnhancedKeyUsageIdentifier function adds a usage identifier object identifier (OID) to the enhanced key usage (EKU) extended property of the certificate.helpviewer_keywords: ["CertAddEnhancedKeyUsageIdentifier","CertAddEnhancedKeyUsageIdentifier function [Security]","_crypto2_certaddenhancedkeyusageidentifier","security.certaddenhancedkeyusageidentifier","wincrypt/CertAddEnhancedKeyUsageIdentifier"]
old-location: security\certaddenhancedkeyusageidentifier.htm
tech.root: SecCrypto
ms.assetid: 1bec8d2f-aa43-4a8b-9414-c3a4e5fcb470
ms.date: 12/05/2018
ms.keywords: CertAddEnhancedKeyUsageIdentifier, CertAddEnhancedKeyUsageIdentifier function [Security], _crypto2_certaddenhancedkeyusageidentifier, security.certaddenhancedkeyusageidentifier, wincrypt/CertAddEnhancedKeyUsageIdentifier
f1_keywords:
- wincrypt/CertAddEnhancedKeyUsageIdentifier
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CertAddEnhancedKeyUsageIdentifier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertAddEnhancedKeyUsageIdentifier function


## -description


The <b>CertAddEnhancedKeyUsageIdentifier</b> function adds a usage identifier <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/e-gly">enhanced key usage</a> (EKU) extended property of the certificate.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the certificate for which the usage identifier is to be added.


### -param pszUsageIdentifier [in]

Specifies the usage identifier OID to add.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Enhanced Key Usage Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>
 

 

