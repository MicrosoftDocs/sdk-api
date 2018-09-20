---
UID: NF:wincrypt.CertFreeCertificateChainEngine
title: CertFreeCertificateChainEngine function
author: windows-sdk-content
description: The CertFreeCertificateChainEngine function frees a certificate trust engine.
old-location: security\certfreecertificatechainengine.htm
tech.root: seccrypto
ms.assetid: 5aebc09d-342d-4938-8a1a-0cbfdc147bb5
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: CertFreeCertificateChainEngine, CertFreeCertificateChainEngine function [Security], _crypto2_certfreecertificatechainengine, security.certfreecertificatechainengine, wincrypt/CertFreeCertificateChainEngine
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
 - CertFreeCertificateChainEngine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertFreeCertificateChainEngine function


## -description


The <b>CertFreeCertificateChainEngine</b> function frees a certificate trust engine.


## -parameters




### -param hChainEngine [in]

Handle of the chain engine to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e173016a-d3d7-42e0-aad8-e738abaf1df9">CertCreateCertificateChainEngine</a>



<a href="cryptography_functions.htm">Certificate Chain Verification Functions</a>
 

 

