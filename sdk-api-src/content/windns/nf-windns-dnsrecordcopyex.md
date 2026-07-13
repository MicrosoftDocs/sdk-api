---
UID: NF:windns.DnsRecordCopyEx
title: DnsRecordCopyEx function (windns.h)
description: The DnsRecordCopyEx function creates a copy of a specified resource record (RR). The DnsRecordCopyEx function is also capable of converting the character encoding during the copy operation.
helpviewer_keywords: ["DnsRecordCopyEx","DnsRecordCopyEx function [DNS]","_dns_dnsrecordcopyex","dns.dnsrecordcopyex","windns/DnsRecordCopyEx"]
old-location: dns\dnsrecordcopyex.htm
tech.root: DNS
ms.assetid: b5a74799-75fc-4489-9efa-c15b2def2ae7
ms.date: 12/05/2018
ms.keywords: DnsRecordCopyEx, DnsRecordCopyEx function [DNS], _dns_dnsrecordcopyex, dns.dnsrecordcopyex, windns/DnsRecordCopyEx
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DnsRecordCopyEx
 - windns/DnsRecordCopyEx
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
 - DnsRecordCopyEx
---

# DnsRecordCopyEx function


## -description

The 
<b>DnsRecordCopyEx</b> function creates a copy of a specified <a href="/windows/desktop/DNS/r-gly">resource record</a> (RR). The 
<b>DnsRecordCopyEx</b> function is also capable of converting the character encoding during the copy operation.

## -parameters

### -param pRecord [in]

A pointer to a <a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a> structure that contains the RR to be copied.

### -param CharSetIn [in]

A <a href="/windows/desktop/api/windnsdef/ne-windnsdef-dns_charset">DNS_CHARSET</a> value that specifies the character encoding of the source RR.

### -param CharSetOut [in]

A <a href="/windows/desktop/api/windnsdef/ne-windnsdef-dns_charset">DNS_CHARSET</a> value that specifies the character encoding required of the destination record.

## -returns

Successful execution returns a pointer to the (newly created) destination record. Otherwise, returns null.

## -remarks

The <i>CharSetIn</i> parameter is used only if the character encoding of the source RR is not specified in <i>pRecord</i>.

## -see-also

<a href="/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda">DNS_RECORD</a>



<a href="/windows/desktop/api/windns/nf-windns-dnsrecordsetcopyex">DnsRecordSetCopyEx</a>