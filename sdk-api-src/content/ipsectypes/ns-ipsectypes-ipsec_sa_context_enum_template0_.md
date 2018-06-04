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

# IPSEC_SA_CONTEXT_ENUM_TEMPLATE0_ structure


## -description


The <b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b>	structure is an enumeration template used to enumerate security association (SA) contexts.


## -struct-fields




### -field localSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a local address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a>.


### -field remoteSubNet

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that specifies a subnet from which SA contexts that contain a remote address will be returned.  This member may be empty.

Acceptable type values for this member are: <b>FWP_UINT32</b>, <a href="https://msdn.microsoft.com/254ee02f-747d-46e4-9851-141db57e1aa7">FWP_BYTE_ARRAY16_TYPE</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff552441">FWP_V4_ADDR_AND_MASK</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff552446">FWP_V6_ADDR_AND_MASK</a>.


## -remarks



<b>IPSEC_SA_CONTEXT_ENUM_TEMPLATE0</b> is a specific implementation of IPSEC_SA_CONTEXT_ENUM_TEMPLATE. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>
 

 

