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

# _RSVP_FILTERSPEC_V4 structure


## -description


The <b>RSVP_FILTERSPEC_V4</b> structure stores information for a FILTERSPEC on an IPv4 address.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC applies, expressed as an <a href="https://msdn.microsoft.com/7e10cc9c-7ed4-449d-aeb9-21e3d75d0224">IN_ADDR_IPV4</a> union.


### -field Unused

Reserved. Set to zero.


### -field Port

TCP port of the socket on which the FILTERSPEC applies.


## -remarks



When working with IPv6 addresses, use <a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a>.




## -see-also




<a href="https://msdn.microsoft.com/7e10cc9c-7ed4-449d-aeb9-21e3d75d0224">IN_ADDR_IPV4</a>



<a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a>
 

 

