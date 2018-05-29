---
UID: NS:windns.__unnamed_struct_30
title: DNS_SRV_DATAW
author: windows-sdk-content
description: The DNS_SRV_DATA structure represents a DNS service (SRV) record as specified in RFC 2782.
old-location: dns\dns_srv_data.htm
old-project: DNS
ms.assetid: 212db7ac-a5e3-4e58-b1c2-0eb551403dfc
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: "*PDNS_SRV_DATA, *PDNS_SRV_DATAW, DNS_SRV_DATA, DNS_SRV_DATA structure [DNS], DNS_SRV_DATAW, PDNS_SRV_DATA, PDNS_SRV_DATA structure pointer [DNS], _dns_dns_srv_data, dns.dns_srv_data, windns/DNS_SRV_DATA, windns/PDNS_SRV_DATA"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DNS_SRV_DATAW, *PDNS_SRV_DATAW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_SRV_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_SRV_DATAW structure


## -description


The 
<b>DNS_SRV_DATA</b> structure represents a DNS service (SRV) record as specified in <a href="http://go.microsoft.com/fwlink/p/?linkid=90381">RFC 2782</a>.


## -struct-fields




### -field pNameTarget

A pointer to a string that represents the target host.


### -field wPriority

The priority of the target host specified in <b>pNameTarget</b>. Lower numbers imply higher priority to clients attempting to use this service.


### -field wWeight

The relative weight of the target host in <b>pNameTarget</b> to other hosts with the same <b>wPriority</b>. The chances of using this host should be proportional to its weight.


### -field wPort

The port used on the target host for this service.


### -field Pad

Reserved for padding. Do not use.


## -remarks



The 
<b>DNS_SRV_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

