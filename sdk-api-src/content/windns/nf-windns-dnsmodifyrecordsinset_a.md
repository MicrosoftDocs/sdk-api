---
UID: NF:windns.DnsModifyRecordsInSet_A
title: DnsModifyRecordsInSet_A function (windns.h)
description: Function adds, modifies or removes a Resource Record (RR) set that may have been previously registered with DNS servers. (DnsModifyRecordsInSet_A)
helpviewer_keywords: ["DnsModifyRecordsInSet", "DnsModifyRecordsInSet function [DNS]", "DnsModifyRecordsInSet_A", "_dns_dnsmodifyrecordsinset", "dns.dnsmodifyrecordsinset", "windns/DnsModifyRecordsInSet", "windns/DnsModifyRecordsInSet_A"]
old-location: dns\dnsmodifyrecordsinset.htm
tech.root: DNS
ms.assetid: 4287b4e1-a7a2-4b73-b5bb-21bc639bae73
ms.date: 12/05/2018
ms.keywords: DnsModifyRecordsInSet, DnsModifyRecordsInSet function [DNS], DnsModifyRecordsInSet_A, DnsModifyRecordsInSet_UTF8, DnsModifyRecordsInSet_W, _dns_dnsmodifyrecordsinset, dns.dnsmodifyrecordsinset, windns/DnsModifyRecordsInSet, windns/DnsModifyRecordsInSet_A, windns/DnsModifyRecordsInSet_UTF8, windns/DnsModifyRecordsInSet_W
req.header: windns.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsModifyRecordsInSet_W (Unicode) and DnsModifyRecordsInSet_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dnsapi.lib
req.dll: Dnsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsModifyRecordsInSet_A
 - windns/DnsModifyRecordsInSet_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dnsapi.dll
api_name:
 - DnsModifyRecordsInSet
 - DnsModifyRecordsInSet_A
 - DnsModifyRecordsInSet_W
 - DnsModifyRecordsInSet_UTF8
---

# DnsModifyRecordsInSet_A function


## -description

The 
<b>DnsModifyRecordsInSet</b> function adds, modifies or removes a Resource Record (RR) set that may have been previously registered with DNS servers.

Like many DNS functions, the 
<b>DnsModifyRecordsInSet</b> function type is implemented in multiple forms to facilitate different character encoding. Based on the character encoding involved, use one of the following functions:
<ul>
<li><b>DnsModifyRecordsInSet_A</b> (_A for ANSI encoding)</li>
<li><b>DnsModifyRecordsInSet_W</b> (_W for Unicode encoding)</li>
<li><b>DnsModifyRecordsInSet_UTF8</b> (_UTF8 for UTF 8 encoding)</li>
</ul>

## -parameters

### -param pAddRecords [in, optional]

A pointer to the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the RRs to be added to the RR set.

### -param pDeleteRecords [in, optional]

A pointer to the 
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the RRs to be deleted from the RR set.

### -param Options [in]

A value that contains a bitmap of <a href="/windows/desktop/DNS/dns-constants">DNS Update  Options</a>. Options can be combined and all options override <b>DNS_UPDATE_SECURITY_USE_DEFAULT</b>.

### -param hCredentials [in, optional]

A handle to the credentials of a specific account. Used when secure dynamic update is required. This parameter is optional.

### -param pExtraList [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param pReserved [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

## -returns

Returns success confirmation upon successful completion. Otherwise, it returns the appropriate DNS-specific error code as defined in Winerror.h.

## -remarks

The 
<b>DnsModifyRecordsInSet</b> function type executes in the following steps.

<ol>
<li>Records specified in <i>pDeleteRecords</i> are deleted. If <i>pDeleteRecords</i> is empty or does not contain records that exist in the current set, the <b>DnsModifyRecordsInSet</b> function goes to the next step.</li>
<li>Records specified in <i>pAddRecords</i> are added. If <i>pAddRecords</i> is empty, the operation completes without adding any records.</li>
</ol>
To add a new record, provide no records in <i>pDeleteRecords</i>, and provide the record to be added in <i>pAddRecords</i>.  To modify a record, specify the record being modified in <i>pDeleteRecords</i>, then add the modified version of that record by placing it in <i>pAddRecords</i>. To delete records, specify only records to be deleted.  Multiple records can be added or deleted in a single call to <b>DnsModifyRecordsInSet</b>; however, the value of the <b>pName</b> member in each <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> must be the same or the call will fail. If a record specified in <i>pAddRecords</i> is already present, no change occurs.

If no server list is specified, the default name server is queried.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsquery_a">DnsQuery</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsreplacerecordseta">DnsReplaceRecordSet</a>
