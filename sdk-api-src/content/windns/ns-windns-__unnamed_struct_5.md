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

# DNS_SOA_DATAW structure


## -description


The 
<b>DNS_SOA_DATA</b> structure represents a DNS start of authority (SOA) record as specified in section 3.3.13 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field pNamePrimaryServer

A pointer to a string that represents the name of the authoritative DNS server for the zone to which the record belongs.


### -field pNameAdministrator

A pointer to a string that represents the name of the responsible party for the zone to which the record belongs.


### -field dwSerialNo

The serial number of the SOA record.


### -field dwRefresh

The time, in seconds, before the zone containing this record should be refreshed.


### -field dwRetry

The time, in seconds, before retrying a failed refresh of the zone to which this record belongs.


### -field dwExpire

The time, in seconds, before an unresponsive zone is no longer authoritative.


### -field dwDefaultTtl

The lower limit on the time, in seconds, that a DNS server or caching resolver are allowed to cache any resource records (RR) from the zone to which this record belongs.


## -remarks



The 
<b>DNS_SOA_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

