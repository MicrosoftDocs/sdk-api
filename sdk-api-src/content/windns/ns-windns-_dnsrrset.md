---
UID: NS:windns._DnsRRSet
title: "_DnsRRSet"
author: windows-driver-content
description: The DNS_RRSET structure contains information about a DNS Resource Record (RR) set.
old-location: dns\dns_rrset.htm
old-project: DNS
ms.assetid: bd87a8db-ca27-490b-85f4-912297b77a2b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PDNS_RRSET, *PDNS_RRSET structure [DNS], DNS_RRSET, DNS_RRSET structure [DNS], _DnsRRSet, dns.dns_rrset, windns/*PDNS_RRSET, windns/DNS_RRSET"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DNS_RRSET, *PDNS_RRSET
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_RRSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DnsRRSet structure


## -description


The <b>DNS_RRSET</b> structure contains information about a DNS Resource Record (RR) set.


## -struct-fields




### -field pFirstRR

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the first DNS RR in the set.


### -field pLastRR

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the last DNS RR in the set.


## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

