---
UID: NF:windns.DnsRecordCopyEx
title: DnsRecordCopyEx function
author: windows-sdk-content
description: The DnsRecordCopyEx function creates a copy of a specified resource record (RR). The DnsRecordCopyEx function is also capable of converting the character encoding during the copy operation.
old-location: dns\dnsrecordcopyex.htm
tech.root: dns
ms.assetid: b5a74799-75fc-4489-9efa-c15b2def2ae7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: DnsRecordCopyEx, DnsRecordCopyEx function [DNS], _dns_dnsrecordcopyex, dns.dnsrecordcopyex, windns/DnsRecordCopyEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsRecordCopyEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsRecordCopyEx function


## -description


The 
<b>DnsRecordCopyEx</b> function creates a copy of a specified <a href="https://msdn.microsoft.com/675287c2-9394-4d32-8ef4-9bb64794d326">resource record</a> (RR). The 
<b>DnsRecordCopyEx</b> function is also capable of converting the character encoding during the copy operation.


## -parameters




### -param pRecord [in]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the RR to be copied.


### -param CharSetIn [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding of the source RR.


### -param CharSetOut [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding required of the destination record.


## -returns



Successful execution returns a pointer to the (newly created) destination record. Otherwise, returns null.




## -remarks



The <i>CharSetIn</i> parameter is used only if the character encoding of the source RR is not specified in <i>pRecord</i>.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a">DnsRecordSetCopyEx</a>
 

 

