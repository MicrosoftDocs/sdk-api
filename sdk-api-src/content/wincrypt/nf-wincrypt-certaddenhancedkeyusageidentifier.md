---
UID: NF:wincrypt.CertAddEnhancedKeyUsageIdentifier
title: CertAddEnhancedKeyUsageIdentifier function
author: windows-sdk-content
description: The CertAddEnhancedKeyUsageIdentifier function adds a usage identifier object identifier (OID) to the enhanced key usage (EKU) extended property of the certificate.
old-location: security\certaddenhancedkeyusageidentifier.htm
old-project: seccrypto
ms.assetid: 1bec8d2f-aa43-4a8b-9414-c3a4e5fcb470
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CertAddEnhancedKeyUsageIdentifier, CertAddEnhancedKeyUsageIdentifier function [Security], _crypto2_certaddenhancedkeyusageidentifier, security.certaddenhancedkeyusageidentifier, wincrypt/CertAddEnhancedKeyUsageIdentifier
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertAddEnhancedKeyUsageIdentifier
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertAddEnhancedKeyUsageIdentifier function


## -description


The <b>CertAddEnhancedKeyUsageIdentifier</b> function adds a usage identifier <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) to the <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">enhanced key usage</a> (EKU) extended property of the certificate.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the certificate for which the usage identifier is to be added.


### -param pszUsageIdentifier [in]

Specifies the usage identifier OID to add.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="cryptography_functions.htm">Enhanced Key Usage Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

