---
UID: NS:windns.__unnamed_struct_7
title: DNS_MINFO_DATAW
author: windows-sdk-content
description: The DNS_MINFO_DATA structure represents a DNS mail information (MINFO) record as specified in section 3.3.7 of RFC 1035.
old-location: dns\dns_minfo_data.htm
old-project: DNS
ms.assetid: cd392b48-734f-462b-b893-855f07c30575
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: "*PDNS_MINFO_DATA, *PDNS_MINFO_DATAW, DNS_MINFO_DATA, DNS_MINFO_DATA structure [DNS], DNS_MINFO_DATAW, PDNS_MINFO_DATA, PDNS_MINFO_DATA structure pointer [DNS], _dns_dns_minfo_data, dns.dns_minfo_data, windns/DNS_MINFO_DATA, windns/PDNS_MINFO_DATA"
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
req.typenames: DNS_MINFO_DATAW, *PDNS_MINFO_DATAW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windns.h
api_name:
 - DNS_MINFO_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# DNS_MINFO_DATAW structure


## -description


The 
<b>DNS_MINFO_DATA</b> structure represents a DNS mail information (MINFO) record as specified in section 3.3.7 of <a href="http://go.microsoft.com/fwlink/p/?linkid=90264">RFC 1035</a>.


## -struct-fields




### -field pNameMailbox

A pointer to a string that represents the <a href="f_gly.htm">fully qualified domain name</a> (FQDN) of the mailbox responsible for the mailing list or mailbox specified in the record's owner name.


### -field pNameErrorsMailbox

A pointer to a string that represents the FQDN of the mailbox to receive error messages related to the mailing list.


## -remarks



The 
<b>DNS_MINFO_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

