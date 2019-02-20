---
UID: NS:windns.__unnamed_struct_26
title: DNS_OPT_DATA
author: windows-sdk-content
description: Represents a DNS Option (OPT) resource record (RR) as specified in section 4 of RFC 2671.
old-location: dns\dns_opt_data.htm
tech.root: DNS
ms.assetid: a8e23127-a625-4206-abe8-0787b4ac0f30
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDNS_OPT_DATA, DNS_OPT_DATA, DNS_OPT_DATA structure [DNS], PDNS_OPT_DATA, PDNS_OPT_DATA structure pointer [DNS], dns.dns_opt_data, windns/DNS_OPT_DATA, windns/PDNS_OPT_DATA"
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
 - DNS_OPT_DATA
product: Windows
targetos: Windows
req.typenames: DNS_OPT_DATA, *PDNS_OPT_DATA
req.redist: 
---

# DNS_OPT_DATA structure


## -description


The <b>DNS_OPT_DATA</b> structure represents a DNS Option  (OPT) resource record (RR) as specified in section 4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=134711">RFC 2671</a>.


## -struct-fields




### -field wDataLength

The length, in bytes, of <b>Data</b>.


### -field wPad

Reserved. Do not use.


### -field size_is

 


### -field size_is.wDataLength

 


### -field Data

A <b>BYTE</b> array that contains variable transport level information as specified in section 4 of <a href="http://go.microsoft.com/fwlink/p/?linkid=134711">RFC 2671</a>.


## -remarks



The 
<b>DNS_OPT_DATA</b> structure is used in conjunction with the 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure to programmatically manage DNS entries.




## -see-also




<a href="https://msdn.microsoft.com/636399be-43a5-4ddf-b652-f8efb81fbf42">DNS Structures</a>



<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>
 

 

