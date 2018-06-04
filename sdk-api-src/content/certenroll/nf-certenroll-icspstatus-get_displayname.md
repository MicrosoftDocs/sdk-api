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

# ICspStatus::get_DisplayName


## -description


The <b>DisplayName</b> property retrieves a string that contains the name of the provider, the algorithm name, and the operations that can be performed by the algorithm.

This property is read-only.


## -parameters


## -remarks



The format of the string returned by this property depends on whether the provider is a CryptoAPI <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP) or a Cryptography API: Next Generation (CNG) provider.<ul>
<li>The format of the string for a CSP is <i>ProviderName(KeyType)</i> where <i>KeyType</i> is either "Signature" or "Encryption".</li>
<li>The format of the string for a CNG provider is <i>AlgorithmName,ProviderName</i> where <i>AlgorithmName</i> can be "Unknown Algorithm".</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>



<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
 

 

