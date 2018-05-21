---
UID: NF:wincrypt.CertFreeCertificateChain
title: CertFreeCertificateChain function
author: windows-driver-content
description: The CertFreeCertificateChain function frees a certificate chain by reducing its reference count. If the reference count becomes zero, memory allocated for the chain is released.
old-location: security\certfreecertificatechain.htm
old-project: SecCrypto
ms.assetid: 5ba181c2-6936-4848-a571-2bb58f46f081
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CertFreeCertificateChain, CertFreeCertificateChain function [Security], _crypto2_certfreecertificatechain, security.certfreecertificatechain, wincrypt/CertFreeCertificateChain
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertFreeCertificateChain
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertFreeCertificateChain function


## -description


The <b>CertFreeCertificateChain</b> function frees a certificate chain by reducing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>. If the reference count becomes zero, memory allocated for the chain is released.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.


## -parameters




### -param pChainContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/609311f4-9cd6-4945-9f93-7266b3fc4a74">CERT_CHAIN_CONTEXT</a> certificate chain context to be freed. If the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> on the context reaches zero, the storage allocated for the context is freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>



<a href="cryptography_functions.htm">Certificate Chain Verification Functions</a>
 

 

