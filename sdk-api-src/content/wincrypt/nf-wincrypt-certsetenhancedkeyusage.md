---
UID: NF:wincrypt.CertSetEnhancedKeyUsage
title: CertSetEnhancedKeyUsage function
author: windows-sdk-content
description: The CertSetEnhancedKeyUsage function sets the enhanced key usage (EKU) property for the certificate.
old-location: security\certsetenhancedkeyusage.htm
tech.root: seccrypto
ms.assetid: 423b0232-846e-4e40-bc42-d30c48c548da
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertSetEnhancedKeyUsage, CertSetEnhancedKeyUsage function [Security], _crypto2_certsetenhancedkeyusage, security.certsetenhancedkeyusage, wincrypt/CertSetEnhancedKeyUsage
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
 - CertSetEnhancedKeyUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CertSetEnhancedKeyUsage
: 
---

# CertSetEnhancedKeyUsage function


## -description


The <b>CertSetEnhancedKeyUsage</b> function sets the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enhanced key usage</a> (EKU) property for the certificate. Use of this function replaces any EKUs associated with the certificate. To add a single EKU usage without changing existing usages, use 
<a href="https://msdn.microsoft.com/1bec8d2f-aa43-4a8b-9414-c3a4e5fcb470">CertAddEnhancedKeyUsageIdentifier</a>. To delete a single EKU usage, use 
<a href="https://msdn.microsoft.com/4fb27073-674c-4bac-9a62-6e33e1a5785e">CertRemoveEnhancedKeyUsageIdentifier</a>.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the specified certificate.


### -param pUsage [in]

Pointer to a <a href="https://msdn.microsoft.com/70ee138a-df94-4fc4-9de5-0d8b7704b890">CERT_ENHKEY_USAGE</a> structure (equivalent to a 
<b>CTL_USAGE</b> structure) that contains an array of EKU <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs) to be set as extended properties of the certificate.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/eda6d875-df62-4f40-8734-a91666dba289">CertGetEnhancedKeyUsage</a>



<a href="cryptography_functions.htm">Enhanced Key Usage Functions</a>
 

 

