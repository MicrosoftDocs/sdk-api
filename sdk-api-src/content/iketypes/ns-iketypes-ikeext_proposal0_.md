---
UID: NS:iketypes.IKEEXT_PROPOSAL0_
title: IKEEXT_PROPOSAL0_
author: windows-sdk-content
description: Is used to store an IKE/AuthIP main mode proposal.
old-location: fwp\ikeext_proposal0.htm
tech.root: FWP
ms.assetid: 59568ef7-12bd-407a-a8ee-9bf261f49883
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IKEEXT_PROPOSAL0, IKEEXT_PROPOSAL0 structure [Filtering], IKEEXT_PROPOSAL0_, fwp.ikeext_proposal0, iketypes/IKEEXT_PROPOSAL0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
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
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_PROPOSAL0
product: Windows
targetos: Windows
req.typenames: IKEEXT_PROPOSAL0
req.redist: 
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
 

 

