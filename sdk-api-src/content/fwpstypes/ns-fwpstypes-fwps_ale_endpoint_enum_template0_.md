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

# FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_ structure


## -description


The <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> structure specifies a template for application layer enforcement
  (ALE) endpoints to be enumerated.
<div class="alert"><b>Note</b>  <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0</b> is a specific version of <b>FWPS_ALE_ENDPOINT_ENUM_TEMPLATE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field localSubNet

The local subnet portion of the enumeration template.


### -field remoteSubNet

The remote subnet portion of the enumeration template.


### -field ipProtocol

The IP protocol portion of the enumeration template.


### -field localPort

The local port portion of the enumeration template.


### -field remotePort

The remote port portion of the enumeration template.


## -remarks



This structure can be used to narrow the results when enumerating endpoints. If used, it is specified
    when the enumeration handle is created by calling 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff550089">FwpsAleEndpointCreateEnumHandle0</a>. Any populated members are used to limit the enumeration results
    returned by 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff551126">FwpsAleEndpointEnum0</a>.




## -see-also




<a href="https://msdn.microsoft.com/5daa3dd4-e499-4a72-b784-8a0e1ef3e92b">
   FwpsAleEndpointCreateEnumHandle0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551126">FwpsAleEndpointEnum0</a>
 

 

