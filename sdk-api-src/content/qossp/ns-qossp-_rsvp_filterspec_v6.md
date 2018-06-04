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

# _RSVP_FILTERSPEC_V6 structure


## -description


The <b>RSVP_FILTERSPEC_V6</b> structure  stores information for a FILTERSPEC on an IPv6 address.


## -struct-fields




### -field Address

IPv4 address for which the FILTERSPEC applies, expressed as an <a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a> structure.


### -field UnUsed

 


### -field Port

TCP port of the socket on which the FILTERSPEC applies.


#### - Unused

Reserved. Set to zero.


## -remarks



When working with IPv4 addresses, use <a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>.




## -see-also




<a href="https://msdn.microsoft.com/e21edb47-c704-415f-901b-7612e5157ab0">IN_ADDR_IPV6</a>



<a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>
 

 

