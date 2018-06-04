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

# _CERT_POLICY_ID structure


## -description


The <b>CERT_POLICY_ID</b> structure contains a list of certificate policies that the certificate expressly supports, together with optional qualifier information pertaining to these policies.

<b>CERT_POLICY_ID</b> is a component of 
<a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a>.


## -struct-fields




### -field cCertPolicyElementId

Number of elements in the <b>rgpszCertPolicyElementId</b> array.
					


### -field rgpszCertPolicyElementId

Array of pointers to policy element identifier strings.


## -see-also




<a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a>
 

 

