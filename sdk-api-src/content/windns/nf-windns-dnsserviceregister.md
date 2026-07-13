---
UID: NF:windns.DnsServiceRegister
title: DnsServiceRegister function
description: Used to register a discoverable service on this device. (DnsServiceRegister)
tech.root: dns
helpviewer_keywords: ["DnsServiceRegister"]
ms.date: 02/14/2019
ms.keywords: DnsServiceRegister
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
 - DnsServiceRegister
 - windns/DnsServiceRegister
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceRegister
---

## -description

Used to register a discoverable service on this device.

## -parameters

### -param pRequest

A pointer to a [DNS_SERVICE_REGISTER_REQUEST](ns-windns-dns_service_register_request.md) structure that contains information about the service to be registered.

### -param pCancel

An optional (it can be `nullptr`) pointer to a [DNS_SERVICE_CANCEL](ns-windns-dns_service_cancel.md) structure that can be used to cancel a pending asynchronous registration operation. If not `nullptr`, then this handle must remain valid until the registration is canceled.

## -returns

If successful, returns **DNS_REQUEST_PENDING**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

This function is asynchronous. The registration callback will be called once the registration succeeds. To deregister the service, call [DnsServiceDeRegister](nf-windns-dnsservicederegister.md).
 
The registration is tied to the lifetime of the calling process. If the process goes away, the service will be automatically deregistered.

## -see-also
