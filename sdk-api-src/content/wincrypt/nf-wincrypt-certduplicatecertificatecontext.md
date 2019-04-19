---
UID: NF:wincrypt.CertDuplicateCertificateContext
title: CertDuplicateCertificateContext function (wincrypt.h)
author: windows-sdk-content
description: Duplicates a certificate context by incrementing its reference count.
old-location: security\certduplicatecertificatecontext.htm
tech.root: SecCrypto
ms.assetid: 589edd25-c8d0-4f93-83b2-9df2ed2e2812
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertDuplicateCertificateContext, CertDuplicateCertificateContext function [Security], _crypto2_certduplicatecertificatecontext, security.certduplicatecertificatecontext, wincrypt/CertDuplicateCertificateContext
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertDuplicateCertificateContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertDuplicateCertificateContext function


## -description


The <b>CertDuplicateCertificateContext</b> function duplicates a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> by incrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure for which the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is incremented.


## -returns



Currently, a copy is not made of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>, and the returned pointer to a context has the same value as the pointer to a context that was input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned. When you have finished using the duplicate context, decrease its reference count by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ea14c494-d1c7-46d0-9d56-fc89a4b4afa9">CertDuplicateCRLContext</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Functions</a>
 

 

