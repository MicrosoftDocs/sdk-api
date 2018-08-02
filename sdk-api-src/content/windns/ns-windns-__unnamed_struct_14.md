---
UID: NS:windns.__unnamed_struct_14
title: DNS_WKS_DATA
author: windows-sdk-content
description: The DNS_WKS_DATA structure represents a DNS well-known services (WKS) record as specified in section 3.4.2 of RFC 1035.
old-location: dns\dns_wks_data.htm
old-project: DNS
ms.assetid: 94477345-74e7-40bf-a75b-e4bf67f1c17b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PDNS_WKS_DATA, DNS_WKS_DATA, DNS_WKS_DATA structure [DNS], PDNS_WKS_DATA, PDNS_WKS_DATA structure pointer [DNS], Transmission Control Protocol (TCP), User Datagram Protocol (UDP), _dns_dns_wks_data, dns.dns_wks_data, windns/DNS_WKS_DATA, windns/PDNS_WKS_DATA"
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
tech.root: 
req.typenames: DNS_WKS_DATA, *PDNS_WKS_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_WKS_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_WKS_DATA structure


## -description


The 
<b>DNS_WKS_DATA</b> structure represents a DNS well-known services (WKS) record as specified in section 3.4.2 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field IpAddress

An <a href="https://msdn.microsoft.com/652012a5-e45d-4ea6-896a-17e8b1ed4a05">IP4_ADDRESS</a> data type that contains the IPv4 address for this resource record (RR).


### -field chProtocol

A value that represents the IP protocol for this RR as defined in <a href="http://go.microsoft.com/fwlink/p/?linkid=107049">RFC 1010</a>.



#### Transmission Control Protocol (TCP) (6)



#### User Datagram Protocol (UDP) (17)


### -field BitMask

A variable-length bitmask whose bits correspond to the port number of well known services offered by the protocol specified in <b>chProtocol</b>. The bitmask has one bit for every port of the supported protocol, but must be a multiple of a <b>BYTE</b>. Bit 0 corresponds to port 1, bit 1 corresponds to port 2, and so forth for a maximum of 1024 bits.


## -remarks



The 
<b>DNS_WKS_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

