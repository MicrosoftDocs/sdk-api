---
UID: NF:wincrypt.CertFreeCertificateContext
title: CertFreeCertificateContext function
author: windows-sdk-content
description: Frees a certificate context by decrementing its reference count. When the reference count goes to zero, CertFreeCertificateContext frees the memory used by a certificate context.
old-location: security\certfreecertificatecontext.htm
old-project: seccrypto
ms.assetid: 7d2f3237-3f8b-4234-b6db-3057384cd89b
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: CertFreeCertificateContext, CertFreeCertificateContext function [Security], _crypto2_certfreecertificatecontext, security.certfreecertificatecontext, wincrypt/CertFreeCertificateContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
 - CertFreeCertificateContext
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertFreeCertificateContext function


## -description


The <b>CertFreeCertificateContext</b> function frees a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a> by decrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>. When the reference count goes to zero, <b>CertFreeCertificateContext</b> frees the memory used by a certificate context.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> to be freed.


## -returns



The function always returns nonzero.




## -see-also




<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>



<a href="cryptography_functions.htm">Certificate Functions</a>
 

 

