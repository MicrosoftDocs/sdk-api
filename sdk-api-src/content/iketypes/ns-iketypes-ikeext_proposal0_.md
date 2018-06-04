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

# IKEEXT_PROPOSAL0_ structure


## -description


The <b>IKEEXT_PROPOSAL0</b> structure is used to store an IKE/AuthIP main mode proposal.


## -struct-fields




### -field cipherAlgorithm

Parameters for the encryption algorithm specified by <a href="https://msdn.microsoft.com/940714a3-d098-4d02-9209-fcf3b24ee4e7">IKEEXT_CIPHER_ALGORITHM0</a>.


### -field integrityAlgorithm

Parameters for the hash algorithm specified by <a href="https://msdn.microsoft.com/231d6ed9-ad41-488c-ad8b-ba64ae73f5b9">IKEEXT_INTEGRITY_ALGORITHM0</a>.


### -field maxLifetimeSeconds

Main mode security association (SA) lifetime in seconds.


### -field dhGroup

The Diffie Hellman group specified by <a href="https://msdn.microsoft.com/ed90c404-f713-4a0d-9698-eece1bfb7dd7">IKEEXT_DH_GROUP</a>.


### -field quickModeLimit

Maximum number of IPsec quick mode SAs that can be generated from this
   main mode SA. 0 (zero) means infinite.


## -remarks



The proposal describes the
various parameters of the IKE/AuthIP main mode SA that is potentially generated
from this proposal.

<b>IKEEXT_PROPOSAL0</b> is a specific implementation of IKEEXT_PROPOSAL. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/940714a3-d098-4d02-9209-fcf3b24ee4e7">IKEEXT_CIPHER_ALGORITHM0</a>



<a href="https://msdn.microsoft.com/ed90c404-f713-4a0d-9698-eece1bfb7dd7">IKEEXT_DH_GROUP</a>



<a href="https://msdn.microsoft.com/231d6ed9-ad41-488c-ad8b-ba64ae73f5b9">IKEEXT_INTEGRITY_ALGORITHM0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

