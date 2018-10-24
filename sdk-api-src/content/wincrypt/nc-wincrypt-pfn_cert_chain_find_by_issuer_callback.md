---
UID: NC:wincrypt.PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK
title: PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK
author: windows-sdk-content
description: An application-defined callback function that allows the application to filter certificates that might be added to the certificate chain.
old-location: security\certchainfindbyissuercallback.htm
tech.root: SecCrypto
ms.assetid: 004c4caa-0063-41a3-8d6d-8b3a769b4112
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CertChainFindByIssuerCallback, PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK, PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK callback, PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK callback function [Security], security.certchainfindbyissuercallback, wincrypt/PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_CHAIN_FIND_BY_ISSUER_CALLBACK callback function


## -description


The <b>CertChainFindByIssuerCallback</b> function is an application-defined callback function that allows the application to filter certificates that might be added to the certificate chain. A pointer to this function is provided in the <b>pfnFindCallback</b> member of the <a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a> structure.


## -parameters




### -param pCert [in]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the certificate in question.


### -param *pvFindArg [in]

A pointer to an application-defined value. This is the same value that was passed in the <i>pvFindArg</i> member of the <a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a> structure.


## -returns



Return <b>TRUE</b> to create a chain for the certificate specified in the <i>pCert</i> parameter, or <b>FALSE</b> otherwise.




## -see-also




<a href="https://msdn.microsoft.com/7dee640e-6bad-4d3c-910f-da928a8682c9">CERT_CHAIN_FIND_BY_ISSUER_PARA</a>



<a href="https://msdn.microsoft.com/698cece8-71a8-4bfa-8ee6-8035a6dcbe05">CertFindChainInStore</a>
 

 

