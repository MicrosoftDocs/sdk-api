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

# DNS_NSEC_DATAW structure


## -description


The <b>DNS_NSEC_DATA</b> structure represents an NSEC resource record (RR) as specified in section 4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -struct-fields




### -field pNextDomainName

A pointer to a string that represents the authoritative owner name of the next domain in the canonical ordering of the zone as specified in section 4.1.1 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


### -field wTypeBitMapsLength

The length, in bytes, of <b>TypeBitMaps</b>.


### -field wPad

Reserved. Do not use.


### -field size_is

 


### -field size_is.wTypeBitMapsLength

 


### -field TypeBitMaps

A <b>BYTE</b> array that contains a bitmap that specifies which RR types are supported by the NSEC RR owner. Each bit in the array corresponds to a <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a> as defined in section in section 4.1.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -remarks



The 
<b>DNS_NSEC_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

