---
UID: NF:wincrypt.CertDuplicateCRLContext
title: CertDuplicateCRLContext function
author: windows-sdk-content
description: The CertDuplicateCRLContext function duplicates a certificate revocation list (CRL) context by incrementing its reference count.
old-location: security\certduplicatecrlcontext.htm
old-project: SecCrypto
ms.assetid: ea14c494-d1c7-46d0-9d56-fc89a4b4afa9
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CertDuplicateCRLContext, CertDuplicateCRLContext function [Security], _crypto2_certduplicatecrlcontext, security.certduplicatecrlcontext, wincrypt/CertDuplicateCRLContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.redist: 
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
 - CertDuplicateCRLContext
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CertDuplicateCRLContext function


## -description


The <b>CertDuplicateCRLContext</b> function duplicates a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context by incrementing its <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a>.


## -parameters




### -param pCrlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> structure for which the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> is being incremented.


## -returns



Currently, a copy is not made of the context, and the returned context is the same as the context that was input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned.




## -see-also




<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>



<a href="cryptography_functions.htm">Certificate Revocation List Functions</a>
 

 

