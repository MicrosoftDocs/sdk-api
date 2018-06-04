---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

