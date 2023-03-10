---
UID: NF:windns.DnsServiceRegisterCancel
title: DnsServiceRegisterCancel function
description: Used to cancel a pending registration operation.
tech.root: dns
helpviewer_keywords: ["DnsServiceRegisterCancel"]
ms.date: 02/14/2019
ms.keywords: DnsServiceRegisterCancel
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
 - DnsServiceRegisterCancel
 - windns/DnsServiceRegisterCancel
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceRegisterCancel
---

## -description

Used to cancel a pending registration operation.

## -parameters

### -param pCancelHandle

A pointer to the [DNS_SERVICE_CANCEL](ns-windns-dns_service_cancel.md) structure that was passed to the [DnsServiceRegister](nf-windns-dnsserviceregister.md) call that is to be cancelled.

## -returns

If successful, returns **ERROR_SUCCESS**. Returns **ERROR_CANCELLED** if the operation was already cancelled, or **ERROR_INVALID_PARAMETER** if the handle is invalid.

## -remarks

## -see-also

