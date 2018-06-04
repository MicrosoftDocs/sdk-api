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

# IKEEXT_SA_ENUM_TEMPLATE0_ structure


## -description


The <b>IKEEXT_SA_ENUM_TEMPLATE0</b> structureis an enumeration template used for enumerating IKE/AuthIP security associations (SAs).


## -struct-fields




### -field localSubNet

Matches SAs whose local address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> for more information.


### -field remoteSubNet

Matches SAs whose remote address is on the specified subnet. Must be of one of the following types.

<ul>
<li>FWP_UINT32</li>
<li>FWP_BYTE_ARRAY16_TYPE</li>
<li>FWP_V4_ADDR_MASK</li>
<li>FWP_V6_ADDR_MASK</li>
</ul>
See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> for more information.


### -field localMainModeCertHash

Matches SAs with a matching local main mode SHA thumbprint.  If none exist, this member will have a length of zero.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> for more information.


## -remarks



<b>IKEEXT_SA_ENUM_TEMPLATE0</b> is a specific implementation of IKEEXT_SA_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

