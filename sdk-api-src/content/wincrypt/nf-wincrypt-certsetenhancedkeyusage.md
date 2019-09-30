---
UID: NF:wincrypt.CertSetEnhancedKeyUsage
title: CertSetEnhancedKeyUsage function (wincrypt.h)
author: windows-sdk-content
description: The CertSetEnhancedKeyUsage function sets the enhanced key usage (EKU) property for the certificate.
old-location: security\certsetenhancedkeyusage.htm
tech.root: SecCrypto
ms.assetid: 423b0232-846e-4e40-bc42-d30c48c548da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertSetEnhancedKeyUsage, CertSetEnhancedKeyUsage function [Security], _crypto2_certsetenhancedkeyusage, security.certsetenhancedkeyusage, wincrypt/CertSetEnhancedKeyUsage
ms.topic: function
f1_keywords:
- wincrypt/CertSetEnhancedKeyUsage
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
- CertSetEnhancedKeyUsage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertSetEnhancedKeyUsage function


## -description


The <b>CertSetEnhancedKeyUsage</b> function sets the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/e-gly">enhanced key usage</a> (EKU) property for the certificate. Use of this function replaces any EKUs associated with the certificate. To add a single EKU usage without changing existing usages, use 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier">CertAddEnhancedKeyUsageIdentifier</a>. To delete a single EKU usage, use 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier">CertRemoveEnhancedKeyUsageIdentifier</a>.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the specified certificate.


### -param pUsage [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure (equivalent to a 
<b>CTL_USAGE</b> structure) that contains an array of EKU <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) to be set as extended properties of the certificate.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certgetenhancedkeyusage">CertGetEnhancedKeyUsage</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Enhanced Key Usage Functions</a>
 

 

