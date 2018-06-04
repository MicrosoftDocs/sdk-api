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

# _RSVP_FILTERSPEC_V4_GPI structure


## -description


The <b>RSVP_FILTERSPEC_V4_GPI</b> structure provides general port identifier information for a given FILTERSPEC.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC general port identifier applies, expressed as an <a href="https://msdn.microsoft.com/7e10cc9c-7ed4-449d-aeb9-21e3d75d0224">IN_ADDR_IPV4</a> union.


### -field GeneralPortId

General Port Identifier for the FILTERSPEC.


## -remarks



When working with IPv6 addresses, use <a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a>.




## -see-also




<a href="https://msdn.microsoft.com/7e10cc9c-7ed4-449d-aeb9-21e3d75d0224">IN_ADDR_IPV4</a>



<a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a>
 

 

