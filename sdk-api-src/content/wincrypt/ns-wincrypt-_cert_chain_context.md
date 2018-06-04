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

# _CERT_CHAIN_CONTEXT structure


## -description


The <b>CERT_CHAIN_CONTEXT</b> structure contains an array of simple certificate chains and a trust status structure that indicates summary validity data on all of the connected simple chains.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field TrustStatus

A structure that indicates the combined trust status of the simple chains array. The structure includes an error status code and an information status code. For information about status code values, see 
<a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a>.


### -field cChain

The number of simple chains in the array.


### -field rgpChain

An array of pointers to simple chain structures. <b>rgpChain</b>[0] is the end certificate simple chain, and <b>rgpChain</b>[<b>cChain</b>–1] is the final chain. If the end certificate is to be considered valid, the final chain must begin with a certificate contained in the root store or an otherwise trusted, self-signed certificate. If the original chain begins with a trusted certificate, there will be only a single simple chain in the array.


### -field cLowerQualityChainContext

The number of chains in the  <b>rgpLowerQualityChainContext</b> array.


### -field rgpLowerQualityChainContext

An array of pointers to CERT_CHAIN_CONTEXT structures. Returned when CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS is set in dwFlags.


### -field fHasRevocationFreshnessTime

A Boolean value set to <b>TRUE</b> if <b>dwRevocationFreshnessTime</b> is available.


### -field dwRevocationFreshnessTime

The largest CurrentTime, in seconds, minus the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list's</a> (CRL's) ThisUpdate of all elements checked.


### -field dwCreateFlags

 


### -field ChainId

 




## -remarks



When a <b>CERT_CHAIN_CONTEXT</b> is built, the first simple chain begins with an end certificate and ends with a self-signed certificate. If that self-signed certificate is not a <a href="https://msdn.microsoft.com/library/windows/hardware/mt484162">root</a> or otherwise trusted certificate, an attempt is made to build a new chain. <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CTLs</a> are used to create the new chain beginning with the self-signed certificate from the original chain as the end certificate of the new chain. This process continues building additional simple chains until the first self-signed certificate is a trusted certificate or until an additional simple chain cannot be built.




## -see-also




<a href="https://msdn.microsoft.com/c130cab4-bf8d-429a-beb7-04cb5d37d466">CERT_SIMPLE_CHAIN</a>



<a href="https://msdn.microsoft.com/af1e1db2-7b53-4491-8317-4abf3568fb03">CERT_TRUST_STATUS</a>



<a href="https://msdn.microsoft.com/8c93036c-0b93-40d4-b0e3-ba1f2fc72db1">CertGetCertificateChain</a>
 

 

