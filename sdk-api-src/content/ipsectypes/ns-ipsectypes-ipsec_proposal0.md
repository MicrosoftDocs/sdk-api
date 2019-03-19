---
UID: NS:ipsectypes.IPSEC_PROPOSAL0_
title: IPSEC_PROPOSAL0 (ipsectypes.h)
author: windows-sdk-content
description: Used to store an IPsec quick mode proposal.
old-location: fwp\ipsec_proposal0_struct.htm
tech.root: fwp
ms.assetid: bc551733-dbba-4d66-8054-fbf4bbfa28b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPSEC_PROPOSAL0, IPSEC_PROPOSAL0 structure [Filtering], fwp.ipsec_proposal0_struct, ipsectypes/IPSEC_PROPOSAL0
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_PROPOSAL0
product: Windows
targetos: Windows
req.typenames: IPSEC_PROPOSAL0
req.redist: 
---

# IPSEC_PROPOSAL0 structure


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
 

 

