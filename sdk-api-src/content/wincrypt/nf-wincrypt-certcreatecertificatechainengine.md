---
UID: NF:wincrypt.CertCreateCertificateChainEngine
title: CertCreateCertificateChainEngine function
author: windows-sdk-content
description: The CertCreateCertificateChainEngine function creates a new, nondefault chain engine for an application.
old-location: security\certcreatecertificatechainengine.htm
tech.root: seccrypto
ms.assetid: e173016a-d3d7-42e0-aad8-e738abaf1df9
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CertCreateCertificateChainEngine, CertCreateCertificateChainEngine function [Security], _crypto2_certcreatecertificatechainengine, security.certcreatecertificatechainengine, wincrypt/CertCreateCertificateChainEngine
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
 - CertCreateCertificateChainEngine
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertCreateCertificateChainEngine function


## -description


The <b>CertCreateCertificateChainEngine</b> function creates a new, nondefault chain engine for an application. A chain engine restricts the certificates in the root store that can be used for verification, restricts the certificate stores to be searched for certificates and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate trust lists</a> (CTLs), sets a time-out limit for searches that involve URLs, and limits the number of certificates checked between checking for a certificate cycle.


## -parameters




### -param pConfig [in]

A pointer to a 
<a href="https://msdn.microsoft.com/9e010eb9-2cbb-4fca-ba5c-4a5a50f23786">CERT_CHAIN_ENGINE_CONFIG</a> data structure that specifies the parameters for the chain engine.


### -param phChainEngine [out]

A pointer to the handle of the chain engine created. When you have finished using the chain engine, release the chain engine by calling the <a href="https://msdn.microsoft.com/5aebc09d-342d-4938-8a1a-0cbfdc147bb5">CertFreeCertificateChainEngine</a> function.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The <i>phChainEngine</i> parameter returns the chain engine handle.




## -see-also




<a href="https://msdn.microsoft.com/9e010eb9-2cbb-4fca-ba5c-4a5a50f23786">CERT_CHAIN_ENGINE_CONFIG</a>



<a href="https://msdn.microsoft.com/5aebc09d-342d-4938-8a1a-0cbfdc147bb5">CertFreeCertificateChainEngine</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Certificate Chain Verification Functions</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

