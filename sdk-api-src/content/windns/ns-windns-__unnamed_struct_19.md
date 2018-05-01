---
UID: NS:windns.__unnamed_struct_19
title: DNS_DHCID_DATA
author: windows-driver-content
description: Represents a DNS Dynamic Host Configuration Protocol Information (DHCID) resource record (RR) as specified in section 3 of RFC 4701.
old-location: dns\dns_dhcid_data.htm
old-project: DNS
ms.assetid: 868846bc-9f63-4bb3-ac8d-cea34232bb41
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PDNS_DHCID_DATA, DNS_DHCID_DATA, DNS_DHCID_DATA structure [DNS], PDNS_DHCID_DATA, PDNS_DHCID_DATA structure pointer [DNS], dns.dns_dhcid_data, windns/DNS_DHCID_DATA, windns/PDNS_DHCID_DATA"
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
req.typenames: DNS_DHCID_DATA, *PDNS_DHCID_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_DHCID_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_DHCID_DATA structure


## -description


The <b>DNS_DHCID_DATA</b> structure represents a DNS Dynamic Host Configuration Protocol Information (DHCID) resource record (RR) as specified in section 3 of <a href="http://go.microsoft.com/fwlink/p/?linkid=125431">RFC 4701</a>.


## -struct-fields




### -field dwByteCount

The length, in bytes, of <b>DHCID</b>.


### -field DHCID

A <b>BYTE</b> array that contains the DHCID client, domain, and SHA-256 digest information as specified in section 4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=134711">RFC 2671</a>.


## -remarks



The 
<b>DNS_DHCID_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

