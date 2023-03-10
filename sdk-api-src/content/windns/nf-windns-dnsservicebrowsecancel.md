---
UID: NF:windns.DnsServiceBrowseCancel
title: DnsServiceBrowseCancel function
description: Used to cancel a running DNS-SD discovery query.
tech.root: dns
helpviewer_keywords: ["DnsServiceBrowseCancel"]
ms.date: 02/14/2019
ms.keywords: DnsServiceBrowseCancel
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dnsapi.dll
req.header: windns.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dnsapi.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
ms.custom: 19H1
f1_keywords:
 - DnsServiceBrowseCancel
 - windns/DnsServiceBrowseCancel
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceBrowseCancel
---

## -description

Used to cancel a running DNS-SD discovery query.

## -parameters

### -param pCancelHandle

A pointer to the [DNS_SERVICE_CANCEL](ns-windns-dns_service_cancel.md) structure that was passed to the [DnsServiceBrowse](nf-windns-dnsservicebrowse.md) call that is to be cancelled.

## -returns

If successful, returns **ERROR_SUCCESS**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

Canceling the query causes one further invocation of the browse callback, with status **ERROR_CANCELLED**.

## -see-also