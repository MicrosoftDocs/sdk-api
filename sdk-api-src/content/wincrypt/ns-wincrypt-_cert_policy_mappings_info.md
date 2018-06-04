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

# _CERT_POLICY_MAPPINGS_INFO structure


## -description


The <b>CERT_POLICY_MAPPINGS_INFO</b> structure provides mapping between the policy OIDs of two domains.


## -struct-fields




### -field cPolicyMapping

Count of the number of elements in the <b>rgPolicyMapping</b> array.


### -field rgPolicyMapping

Array of 
<a href="https://msdn.microsoft.com/6270888a-1c61-472d-8ec7-10c24b890220">CERT_POLICY_MAPPING</a> structures. Each element of this array provides pair of OIDs mapping the identifies of one domain to identifiers in the other domain.

