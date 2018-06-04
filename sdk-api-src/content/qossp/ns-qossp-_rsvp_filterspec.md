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

# _RSVP_FILTERSPEC structure


## -description


The <b>RSVP_FILTERSPEC</b> structure provides RSVP FILTERSPEC information.


## -struct-fields




### -field Type

Specifies the type of FILTERSPEC using the <b>FilterSpec</b> enumeration.


### -field FilterSpecV4

IPv4 FILTERSPEC information, provided in the form of a <a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a> structure.


### -field FilterSpecV6

IPv6 FILTERSPEC information, provided in the form of a <a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a> structure.


### -field FilterSpecV6Flow

IPv6 FILTERSPEC flow information, provided in the form of a <a href="https://msdn.microsoft.com/5bca12be-5bc4-40b2-bc72-52cf0297821b">RSVP_FILTERSPEC_V6_FLOW</a> structure.


### -field FilterSpecV4Gpi

IPv4 FILTERSPEC general port ID information, provided in the form of a <a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a> structure.


### -field FilterSpecV6Gpi

IPv6 FILTERSPEC general port ID information, provided in the form of a <a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/038edc41-7324-4c5a-8172-c958cee05d5e">RSVP_FILTERSPEC_V4</a>



<a href="https://msdn.microsoft.com/bedb3526-700c-4c99-ba02-19389a78acf8">RSVP_FILTERSPEC_V4_GPI</a>



<a href="https://msdn.microsoft.com/7e567714-1d91-4dd4-a560-2b57876c837c">RSVP_FILTERSPEC_V6</a>



<a href="https://msdn.microsoft.com/5bca12be-5bc4-40b2-bc72-52cf0297821b">RSVP_FILTERSPEC_V6_FLOW</a>



<a href="https://msdn.microsoft.com/ede040f4-4858-42d8-a4b5-af6e79c036d7">RSVP_FILTERSPEC_V6_GPI</a>
 

 

