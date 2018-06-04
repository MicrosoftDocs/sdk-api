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

# IPSEC_PROPOSAL0_ structure


## -description


The <b>IPSEC_PROPOSAL0</b> structure is used to store an IPsec quick mode proposal.


## -struct-fields




### -field lifetime

Lifetime of the IPsec security association (SA) as specified by <a href="https://msdn.microsoft.com/9ade5a9a-5c48-4a94-bb35-77f9866e8e6f">IPSEC_SA_LIFETIME0</a>. Cannot be zero.


### -field numSaTransforms

Number of IPsec SA transforms. The only possible values are 1 and 2. Use 2 only when specifying AH plus ESP transforms.


### -field saTransforms

Array of IPsec SA transforms as specified by <a href="https://msdn.microsoft.com/1cf64805-e79d-4599-addf-0ad24d7d900e">IPSEC_SA_TRANSFORM0</a>.


### -field pfsGroup

Perfect forward secrecy (PFS) group of the IPsec SA as specified by <a href="https://msdn.microsoft.com/0f0ea028-859b-42ca-a4e3-fe23f0836883">IPSEC_PFS_GROUP</a>.


## -remarks



The proposal describes the
various parameters of the IPsec SA that is potentially generated from this
proposal.

<b>IPSEC_PROPOSAL0</b> is a specific implementation of IPSEC_PROPOSAL. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/0f0ea028-859b-42ca-a4e3-fe23f0836883">IPSEC_PFS_GROUP</a>



<a href="https://msdn.microsoft.com/9ade5a9a-5c48-4a94-bb35-77f9866e8e6f">IPSEC_SA_LIFETIME0</a>



<a href="https://msdn.microsoft.com/1cf64805-e79d-4599-addf-0ad24d7d900e">IPSEC_SA_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

