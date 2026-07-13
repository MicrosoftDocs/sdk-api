---
UID: NF:windns.DnsReplaceRecordSetA
title: DnsReplaceRecordSetA function (windns.h)
description: Replaces an existing resource record (RR) set. (DnsReplaceRecordSetA)
helpviewer_keywords: ["DnsReplaceRecordSetA", "windns/DnsReplaceRecordSetA"]
old-location: dns\dnsreplacerecordset.htm
tech.root: DNS
ms.assetid: 7b99f440-72fa-4cf4-9267-98f436e99a50
ms.date: 12/05/2018
ms.keywords: DnsReplaceRecordSet, DnsReplaceRecordSet function [DNS], DnsReplaceRecordSetA, DnsReplaceRecordSetUTF8, DnsReplaceRecordSetW, _dns_dnsreplacerecordset, dns.dnsreplacerecordset, windns/DnsReplaceRecordSet, windns/DnsReplaceRecordSetA, windns/DnsReplaceRecordSetUTF8, windns/DnsReplaceRecordSetW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsReplaceRecordSetA
 - windns/DnsReplaceRecordSetA
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
 - DnsReplaceRecordSet
 - DnsReplaceRecordSetW
 - DnsReplaceRecordSetA
 - DnsReplaceRecordSetUTF8
---

# DnsReplaceRecordSetA function


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
<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the RR set that replaces the existing set. The specified RR set is replaced with the contents of <i>pNewSet</i>. To delete a RR set, specify the set in <i>pNewSet</i>, but set <i>RDATA</i> to <b>NULL</b>.

### -param Options [in]

A value that contains a bitmap of <a href="/windows/desktop/DNS/dns-constants">DNS Update  Options</a>. Options can be combined and all options override <b>DNS_UPDATE_SECURITY_USE_DEFAULT</b>.

### -param hContext [in, optional]

The handle to the credentials of a specific account. Used when secure dynamic update is required. This parameter is optional.

### -param pExtraInfo [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

### -param pReserved [in, out, optional]

This parameter is reserved for future use and must be set to <b>NULL</b>.

## -returns

Returns success confirmation upon successful completion. Otherwise, returns the appropriate DNS-specific error code as defined in Winerror.h.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsmodifyrecordsinset_a">DnsModifyRecordsInSet</a>

## -remarks

> [!NOTE]
> The windns.h header defines DnsReplaceRecordSet as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
