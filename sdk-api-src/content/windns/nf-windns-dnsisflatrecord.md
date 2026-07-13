---
UID: NF:windns.DnsIsFlatRecord
title: DnsIsFlatRecord
description: Determines whether a record has been flat-read (that is, it's just a data buffer), or whether it has been parsed into its corresponding struct format.
ms.date: 06/23/2025
tech.root: DNS
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - windns.h
api_name:
 - DnsIsFlatRecord
f1_keywords:
 - DnsIsFlatRecord
 - windns/DnsIsFlatRecord
dev_langs:
 - c++
helpviewer_keywords:
 - DnsIsFlatRecord
---

## -description

Determines whether a record has been flat-read (that is, it's just a data buffer), or whether it has been parsed into its corresponding struct format.

## -parameters

### -param pRecord

Type: \_In\_ **[PDNS_RECORD](/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda)**

A pointer to the [DNS_RECORD](/windows/win32/api/windnsdef/ns-windnsdef-dns_recorda) structure to query about.

### -param ullFlags

Type: \_In\_ **[ULONG64](/windows/win32/winprog/windows-data-types)**

Currently unused; exists for forward compatibility.

### -param pfFlat

Type: \_Out\_ **[BOOL](/windows/win32/winprog/windows-data-types)\***

On completion of the function, if the record has been flat-read (that is, it's just a data buffer), then the value pointed to by *pfFlat* is `TRUE`; if the record has been parsed into its corresponding struct format, then the value pointed to by *pfFlat* is `FALSE`.

## -returns

On successful completion, returns a success confirmation. Otherwise, returns the appropriate DNS-specific error code, as defined in `winerror.h`.

## -remarks

## -see-also
