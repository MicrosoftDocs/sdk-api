---
UID: NF:windns.DnsServiceDeRegister
title: DnsServiceDeRegister function
description: Used to remove a registered service.
tech.root: dns
helpviewer_keywords: ["DnsServiceDeRegister"]
ms.date: 02/14/2019
ms.keywords: DnsServiceDeRegister
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
 - DnsServiceDeRegister
 - windns/DnsServiceDeRegister
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
api_location:
 - windns.h
api_name:
 - DnsServiceDeRegister
---

## -description

Used to remove a registered service.

## -parameters

### -param pRequest

A pointer to the [DNS_SERVICE_REGISTER_REQUEST](ns-windns-dns_service_register_request.md) structure that was used to register the service.

### -param pCancel

Must be `nullptr`.

## -returns

If successful, returns **DNS_REQUEST_PENDING**; otherwise, returns the appropriate DNS-specific error code as defined in `Winerror.h`. For extended error information, call [GetLastError](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

This function is asynchronous. The callback will be invoked when the deregistration is completed, with a copy of the [DNS_SERVICE_INSTANCE](ns-windns-dns_service_instance.md) structure that was passed to [DnsServiceRegister](nf-windns-dnsserviceregister.md) when the service was registered.

## -see-also