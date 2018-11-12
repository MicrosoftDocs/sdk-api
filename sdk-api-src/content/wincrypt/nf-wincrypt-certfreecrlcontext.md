---
UID: NF:wincrypt.CertFreeCRLContext
title: CertFreeCRLContext function
author: windows-sdk-content
description: Frees a certificate revocation list (CRL) context by decrementing its reference count.
old-location: security\certfreecrlcontext.htm
tech.root: seccrypto
ms.assetid: 19a590a5-bd39-4bbe-ad86-4e648baa1ba8
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CertFreeCRLContext, CertFreeCRLContext function [Security], _crypto2_certfreecrlcontext, security.certfreecrlcontext, wincrypt/CertFreeCRLContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CertFreeCRLContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFreeCRLContext function


## -description


The <b>CertFreeCRLContext</b> function frees a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context by decrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>. When the reference count goes to zero, <b>CertFreeCRLContext</b> frees the memory used by a CRL <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.


## -parameters




### -param pCrlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> to be freed.


## -returns



The function always returns <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="cryptography_functions.htm">Certificate Revocation List Functions</a>
 

 

