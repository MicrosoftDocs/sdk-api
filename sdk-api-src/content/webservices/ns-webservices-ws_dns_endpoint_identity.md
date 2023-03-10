---
UID: NS:webservices._WS_DNS_ENDPOINT_IDENTITY
title: WS_DNS_ENDPOINT_IDENTITY (webservices.h)
description: Type for specifying an endpoint identity represented by a DNS name.
helpviewer_keywords: ["WS_DNS_ENDPOINT_IDENTITY","WS_DNS_ENDPOINT_IDENTITY structure [Web Services for Windows]","webservices/WS_DNS_ENDPOINT_IDENTITY","wsw.ws_dns_endpoint_identity"]
old-location: wsw\ws_dns_endpoint_identity.htm
tech.root: wsw
ms.assetid: 09dea451-68ae-4052-8563-30f15c1335d6
ms.date: 12/05/2018
ms.keywords: WS_DNS_ENDPOINT_IDENTITY, WS_DNS_ENDPOINT_IDENTITY structure [Web Services for Windows], webservices/WS_DNS_ENDPOINT_IDENTITY, wsw.ws_dns_endpoint_identity
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_DNS_ENDPOINT_IDENTITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_DNS_ENDPOINT_IDENTITY
 - webservices/_WS_DNS_ENDPOINT_IDENTITY
 - WS_DNS_ENDPOINT_IDENTITY
 - webservices/WS_DNS_ENDPOINT_IDENTITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_DNS_ENDPOINT_IDENTITY
---

# WS_DNS_ENDPOINT_IDENTITY structure


## -description

Type for specifying an endpoint identity represented by a DNS name.

## -struct-fields

### -field identity

The base type from which this type and all other endpoint identity types derive.

### -field dns

The DNS name of the endpoint that is represented by this endpoint identity.
                    The acceptable forms of the name are as defined by <a href="https://datatracker.ietf.org/doc/html/rfc1035">RFC 1035</a>.
                    In particular, they include both a simple machine name as well as a fully qualified domain name (FQDN).

