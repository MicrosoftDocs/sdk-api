---
UID: NS:windns.__unnamed_struct_21
title: DNS_NSEC_DATAA
author: windows-driver-content
description: Represents an NSEC resource record (RR) as specified in section 4 of RFC 4034.
old-location: dns\dns_nsec_data.htm
old-project: DNS
ms.assetid: ea446732-bc6a-4597-b164-11bfd77c07f2
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PDNS_NSEC_DATA, *PDNS_NSEC_DATAA, DNS_NSEC_DATA, DNS_NSEC_DATA structure [DNS], DNS_NSEC_DATAA, PDNS_NSEC_DATA, PDNS_NSEC_DATA structure pointer [DNS], dns.dns_nsec_data, windns/DNS_NSEC_DATA, windns/PDNS_NSEC_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DNS_NSEC_DATAA, *PDNS_NSEC_DATAA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_NSEC_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_NSEC_DATAA structure


## -description


The <b>DNS_NSEC_DATA</b> structure represents an NSEC resource record (RR) as specified in section 4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -struct-fields




### -field pNextDomainName

A pointer to a string that represents the authoritative owner name of the next domain in the canonical ordering of the zone as specified in section 4.1.1 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


### -field wTypeBitMapsLength

The length, in bytes, of <b>TypeBitMaps</b>.


### -field wPad

Reserved. Do not use.


### -field TypeBitMaps

A <b>BYTE</b> array that contains a bitmap that specifies which RR types are supported by the NSEC RR owner. Each bit in the array corresponds to a <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Record Type</a> as defined in section in section 4.1.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=107052">RFC 4034</a>.


## -remarks



The 
<b>DNS_NSEC_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

