---
UID: NS:windns._DnsRecordFlags
title: "_DnsRecordFlags"
author: windows-sdk-content
description: The DNS_RECORD_FLAGS structure is used to set flags for use in the DNS_RECORD structure.
old-location: dns\dns_record_flags.htm
old-project: DNS
ms.assetid: 53c1c8bc-20b0-4b15-b2b6-9c9854f73ee3
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DNS_RECORD_FLAGS, DNS_RECORD_FLAGS structure [DNS], _DnsRecordFlags, _dns_dns_record_flags, dns.dns_record_flags, windns/DNS_RECORD_FLAGS
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
req.typenames: DNS_RECORD_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Windns.h
api_name:
-	DNS_RECORD_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _DnsRecordFlags structure


## -description



			The 
<b>DNS_RECORD_FLAGS</b> structure is used to set flags for use in the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure.


## -struct-fields




### -field Section

A <a href="https://msdn.microsoft.com/d51ef2c7-c2bb-4eed-a026-a559460352b6">DNS_SECTION</a> value that specifies the section of interest returned from the 
<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> function call.


### -field Delete

Reserved. Do not use.


### -field CharSet

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character set used in the associated function call.
					


### -field Unused

Reserved. Do not use.


### -field Reserved

Reserved. Do not use.


## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

