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

# _RSVP_FILTERSPEC_V6_GPI structure


## -description


The <b>RSVP_FILTERSPEC_V6_GPI</b> structure provides general port identifier information for a given FILTERSPEC on an IPv6 address.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC general port identifier applies, expressed as an <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a> structure.


### -field GeneralPortId

General Port Identifier for the FILTERSPEC.


## -remarks



When working with IPv4 addresses, use <a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>.




## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>



<a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>
 

 

