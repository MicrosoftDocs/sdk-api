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

# _TC_GEN_FILTER structure


## -description


The 
<b>TC_GEN_FILTER</b> structure creates a filter that matches a certain set of packet attributes or criteria, which can subsequently be used to associate packets that meet the attribute criteria with a particular flow. The 
<b>TC_GEN_FILTER</b> structure uses its <b>AddressType</b> member to indicate a specific filter type to apply to the filter.


## -struct-fields




### -field AddressType

Defines the filter type to be applied with the filter, as defined in Ntddndis.h. With the designation of a specific filter in <b>AddressType</b>, the generic filter structure 
<b>TC_GEN_FILTER</b> provides a specific filter type.


### -field PatternSize

Size of the <b>Pattern</b> member, in bytes.


### -field Pattern

Indicates the specific format of the pattern to be applied to the filter, such as 
<a href="https://msdn.microsoft.com/c8c3bd92-8120-4a3b-af8b-0a2c0a9bee0f">IP_PATTERN</a>. The pattern specifies which bits of a given packet should be evaluated when determining whether a packet is included in the filter.


### -field Mask

A bitmask applied to the bits designated in the <b>Pattern</b> member. The application of the <b>Mask</b> member to the <b>Pattern</b> member determines which bits in the <b>Pattern</b> member are significant (should be applied to the filter criteria). Note that the <b>Mask</b> member must be of the same type as the <b>Pattern</b> member.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/c8c3bd92-8120-4a3b-af8b-0a2c0a9bee0f">IP_PATTERN</a>
 

 

