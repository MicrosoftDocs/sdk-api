---
UID: NS:windns.__unnamed_struct_6
title: DNS_SOA_DATAA (windns.h)
author: windows-sdk-content
description: The DNS_SOA_DATA structure represents a DNS start of authority (SOA) record as specified in section 3.3.13 of RFC 1035.
old-location: dns\dns_soa_data.htm
tech.root: DNS
ms.assetid: 715cbb70-91fe-47ac-a713-1fe0701d4f8c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDNS_SOA_DATA, *PDNS_SOA_DATAA, DNS_SOA_DATA, DNS_SOA_DATA structure [DNS], DNS_SOA_DATAA, PDNS_SOA_DATA, PDNS_SOA_DATA structure pointer [DNS], _dns_dns_soa_data, dns.dns_soa_data, windns/DNS_SOA_DATA, windns/PDNS_SOA_DATA"
ms.topic: struct
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_SOA_DATA
product: Windows
targetos: Windows
req.typenames: DNS_SOA_DATAA, *PDNS_SOA_DATAA
req.redist: 
ms.custom: 19H1
---

# DNS_SOA_DATAA structure


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
 

 

