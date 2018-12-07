---
UID: NF:windns.DnsReplaceRecordSetUTF8
title: DnsReplaceRecordSetUTF8 function
author: windows-sdk-content
description: Replaces an existing resource record (RR) set.
old-location: dns\dnsreplacerecordset.htm
tech.root: dns
ms.assetid: 7b99f440-72fa-4cf4-9267-98f436e99a50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DnsReplaceRecordSet, DnsReplaceRecordSet function [DNS], DnsReplaceRecordSetA, DnsReplaceRecordSetUTF8, DnsReplaceRecordSetW, _dns_dnsreplacerecordset, dns.dnsreplacerecordset, windns/DnsReplaceRecordSet, windns/DnsReplaceRecordSetA, windns/DnsReplaceRecordSetUTF8, windns/DnsReplaceRecordSetW
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
req.unicode-ansi: DnsReplaceRecordSetA (Unicode) and DnsReplaceRecordSetW (ANSI)
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
 - DnsReplaceRecordSet
 - DnsReplaceRecordSetW
 - DnsReplaceRecordSetA
 - DnsReplaceRecordSetUTF8
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsReplaceRecordSetUTF8 function


## -description


The 
<b>DnsReplaceRecordSet</b> function type replaces an existing resource record (RR) set. Like many DNS functions, the 
<b>DnsReplaceRecordSet</b> function type is implemented in multiple forms to facilitate different character encoding, which is indicated by a suffix. Based on the character encoding involved, use one of the following functions:

<b>DnsReplaceRecordSetA</b> (_A for ANSI encoding)

<b>DnsReplaceRecordSetW</b> (_W for Unicode encoding)

<b>DnsReplaceRecordSetUTF8</b> (_UTF8 for UTF 8 encoding)

Be aware of the lack of an underscore between the function type name and its suffix. If the 
<b>DnsReplaceRecordSet</b> function type is called without its suffix (A, W, or UTF8), a compiler error will occur.


## -parameters




### -param pReplaceSet [in]

A pointer to a 
<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a> structure that contains the RR set that replaces the existing set. The specified RR set is replaced with the contents of <i>pNewSet</i>. To delete a RR set, specify the set in <i>pNewSet</i>, but set <i>RDATA</i> to <b>NULL</b>.


### -param Options [in]

A value that contains a bitmap of <a href="https://msdn.microsoft.com/95bc9193-7962-498a-9abd-c4718ac35f0f">DNS Update  Options</a>. Options can be combined and all options override <b>DNS_UPDATE_SECURITY_USE_DEFAULT</b>.


### -param hContext [in, optional]

The handle to the credentials of a specific account. Used when secure dynamic update is required. This parameter is optional.


### -param pExtraInfo [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


### -param pReserved [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.


## -returns



Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/ab7b96a5-346f-4e01-bb2a-885f44764590">DNS_RECORD</a>



<a href="https://msdn.microsoft.com/4287b4e1-a7a2-4b73-b5bb-21bc639bae73">DnsModifyRecordsInSet</a>
 

 

