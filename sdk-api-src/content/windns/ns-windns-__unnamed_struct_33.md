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

# DNS_NAPTR_DATAA structure


## -description


The 
<b>DNS_NAPTR_DATA</b> structure represents a Naming Authority Pointer (NAPTR) DNS Resource Record (RR) as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


## -struct-fields




### -field wOrder

 A value that determines the NAPTR RR processing order as defined in section 2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field wPreference

A value that determines the NAPTR RR processing  order  for records with the same <b>wOrder</b> value as defined in section 2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pFlags

A pointer to a string  that represents a set of NAPTR RR flags which determine the interpretation and processing of NAPTR record fields as defined in section 2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pService

A pointer to a string that represents the available services in this rewrite path as defined in section 2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pRegularExpression

A pointer to a string that represents a substitution expression as defined in sections 2 and 3 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


### -field pReplacement

A pointer to a string that represents the next NAPTR query name as defined in section 2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107024">RFC 2915</a>.


## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

