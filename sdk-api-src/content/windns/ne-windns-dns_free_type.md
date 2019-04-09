---
UID: NE:windns.__unnamed_enum_1
title: DNS_FREE_TYPE (windns.h)
author: windows-sdk-content
description: The DNS_FREE_TYPE enumeration specifies the type of data to free.
old-location: dns\dns_free_type.htm
tech.root: DNS
ms.assetid: 976982a1-08f1-4c67-b823-1eea34f0c643
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DNS_FREE_TYPE, DNS_FREE_TYPE enumeration [DNS], DnsFreeFlat, DnsFreeParsedMessageFields, DnsFreeRecordList, dns.dns_free_type, windns/DNS_FREE_TYPE, windns/DnsFreeFlat, windns/DnsFreeParsedMessageFields, windns/DnsFreeRecordList
ms.topic: enum
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
 - DNS_FREE_TYPE
product: Windows
targetos: Windows
req.typenames: DNS_FREE_TYPE
req.redist: 
---

# DNS_FREE_TYPE enumeration


## -description


The <b>DNS_FREE_TYPE</b> enumeration specifies the type of data to free.


## -enum-fields




### -field DnsFreeFlat

The data freed is a flat structure.


### -field DnsFreeRecordList

The data freed is a Resource Record list, and includes subfields of the <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure. Resources freed include structures returned by the <a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a> and <a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a> functions.


### -field DnsFreeParsedMessageFields

The data freed is a parsed message field.


## -see-also




<a href="https://msdn.microsoft.com/6ab53b19-7838-4e9f-9923-96a9267d2dbb">DNS Enumerations</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/3d810b76-cea1-4904-9b5a-c2566b332c2c">DnsQuery</a>



<a href="https://msdn.microsoft.com/83de7df8-7e89-42fe-b609-1dc173afc9df">DnsQueryConfig</a>



<a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a>
 

 

