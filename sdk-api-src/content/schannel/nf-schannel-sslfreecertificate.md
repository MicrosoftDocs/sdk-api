---
UID: NF:schannel.SslFreeCertificate
title: SslFreeCertificate function (schannel.h)
author: windows-sdk-content
description: Frees a certificate that was allocated by a previous call to the SslCrackCertificate function.
old-location: security\sslfreecertificate.htm
tech.root: SecAuthN
ms.assetid: bf643ece-fe79-4f6e-a216-108fce6757a4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SslFreeCertificate, SslFreeCertificate function [Security], schannel/SslFreeCertificate, security.sslfreecertificate
ms.topic: function
req.header: schannel.h
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
req.lib: 
req.dll: Schannel.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Schannel.dll
api_name:
 - SslFreeCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SslFreeCertificate function


## -description


<p class="CCE_Message">[The <b>SslFreeCertificate</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function.]

Frees a certificate that was allocated by a previous call to the <a href="https://msdn.microsoft.com/e5ffeebb-0b09-4f0a-b2dc-75fb2a3af7ed">SslCrackCertificate</a> function.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Schannel.dll.


## -parameters




### -param pCertificate [in]

The certificate to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e5ffeebb-0b09-4f0a-b2dc-75fb2a3af7ed">SslCrackCertificate</a>
 

 

