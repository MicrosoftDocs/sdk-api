---
UID: NF:windns.DnsRecordSetCopyEx
title: DnsRecordSetCopyEx function
author: windows-sdk-content
description: The DnsRecordSetCopyEx function creates a copy of a specified resource record set. The DnsRecordSetCopyEx function is also capable of converting the character encoding during the copy operation.
old-location: dns\dnsrecordsetcopyex.htm
old-project: DNS
ms.assetid: bdf9d6b4-b9d7-4886-8ea6-1e1f4dbcc99a
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: DnsRecordSetCopyEx, DnsRecordSetCopyEx function [DNS], _dns_dnsrecordsetcopyex, dns.dnsrecordsetcopyex, windns/DnsRecordSetCopyEx
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DNS_FREE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dnsapi.dll
api_name:
-	DnsRecordSetCopyEx
product: Windows
targetos: Windows
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DnsRecordSetCopyEx function


## -description


The 
<b>DnsRecordSetCopyEx</b> function creates a copy of a specified resource record set. The 
<b>DnsRecordSetCopyEx</b> function is also capable of converting the character encoding during the copy operation.


## -parameters




### -param pRecordSet [in]

A pointer to a <a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the resource record set to be copied.


### -param CharSetIn [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding of the source resource record set.


### -param CharSetOut [in]

A <a href="https://msdn.microsoft.com/2674a4e5-c3e2-4a25-bd6f-1fc6b4db3012">DNS_CHARSET</a> value that specifies the character encoding required of the destination record set.


## -returns



Successful execution returns a pointer to the newly created destination record set. Otherwise, it returns null.




## -remarks



The <i>CharSetIn</i> parameter is used only if the character encoding of the source resource record set is not specified in <i>pRecordSet</i>.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/b5a74799-75fc-4489-9efa-c15b2def2ae7">DnsRecordCopyEx</a>
 

 

