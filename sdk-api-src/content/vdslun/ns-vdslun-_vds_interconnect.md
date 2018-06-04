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

# _VDS_INTERCONNECT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the address 
   data of a physical interconnect.


## -struct-fields




### -field m_addressType


      The interconnect address type enumerated by 
      <a href="https://msdn.microsoft.com/20d75585-a80c-49bc-9f9c-5aae8e5f2c21">VDS_INTERCONNECT_ADDRESS_TYPE</a>.


### -field m_cbPort

The size of the interconnect address data for the LUN port (<b>m_pbPort</b>), in bytes.


### -field m_pbPort

Pointer to the interconnect address data for the LUN port.


### -field m_cbAddress


      The size of the interconnect address data for the LUN (<b>m_pbAddress</b>), in bytes.


### -field m_pbAddress

Pointer to the interconnect address data for the LUN.


## -remarks




    The <a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a> structure includes this 
    structure as a member to specify an interconnect by which a LUN can be accessed.




## -see-also




<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/20d75585-a80c-49bc-9f9c-5aae8e5f2c21">VDS_INTERCONNECT_ADDRESS_TYPE</a>



<a href="https://msdn.microsoft.com/6ad7ec27-add1-4f1e-aa01-6f43c75b7ad9">VDS_LUN_INFORMATION</a>
 

 

