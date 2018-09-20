---
UID: NF:wincrypt.CertRemoveEnhancedKeyUsageIdentifier
title: CertRemoveEnhancedKeyUsageIdentifier function
author: windows-sdk-content
description: The CertRemoveEnhancedKeyUsageIdentifier function removes a usage identifier object identifier (OID) from the enhanced key usage (EKU) extended property of the certificate.
old-location: security\certremoveenhancedkeyusageidentifier.htm
tech.root: seccrypto
ms.assetid: 4fb27073-674c-4bac-9a62-6e33e1a5785e
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CertRemoveEnhancedKeyUsageIdentifier, CertRemoveEnhancedKeyUsageIdentifier function [Security], _crypto2_certremoveenhancedkeyusageidentifier, security.certremoveenhancedkeyusageidentifier, wincrypt/CertRemoveEnhancedKeyUsageIdentifier
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - CertRemoveEnhancedKeyUsageIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertRemoveEnhancedKeyUsageIdentifier function


## -description


The <b>CertRemoveEnhancedKeyUsageIdentifier</b> function removes a usage identifier <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) from the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enhanced key usage</a> (EKU) extended property of the certificate.


## -parameters




### -param pCertContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the certificate for which the usage identifier OID is to be removed.


### -param pszUsageIdentifier [in]

A pointer to the usage identifier OID to remove.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="cryptography_functions.htm">Enhanced Key Usage Functions</a>
 

 

