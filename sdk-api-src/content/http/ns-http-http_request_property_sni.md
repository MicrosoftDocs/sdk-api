---
UID: NS:http._HTTP_REQUEST_PROPERTY_SNI
title: HTTP_REQUEST_PROPERTY_SNI
description: Used to check what domain the client requested when opening a TLS connection.
ms.date: 09/19/2025
tech.root: http
targetos: Windows
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: http.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: HTTP_REQUEST_PROPERTY_SNI, *PHTTP_REQUEST_PROPERTY_SNI
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - _HTTP_REQUEST_PROPERTY_SNI
 - PHTTP_REQUEST_PROPERTY_SNI
 - HTTP_REQUEST_PROPERTY_SNI
f1_keywords:
 - _HTTP_REQUEST_PROPERTY_SNI
 - http/_HTTP_REQUEST_PROPERTY_SNI
 - PHTTP_REQUEST_PROPERTY_SNI
 - http/PHTTP_REQUEST_PROPERTY_SNI
 - HTTP_REQUEST_PROPERTY_SNI
 - http/HTTP_REQUEST_PROPERTY_SNI
dev_langs:
 - c++
helpviewer_keywords:
 - _HTTP_REQUEST_PROPERTY_SNI
---

## -description

Used to check what domain the client requested when opening a TLS connection.

## -struct-fields

### -field Hostname[HTTP_REQUEST_PROPERTY_SNI_HOST_MAX_LENGTH + 1]

Type: **[WCHAR](/windows/win32/winprog/windows-data-types)\[HTTP_REQUEST_PROPERTY_SNI_HOST_MAX_LENGTH + 1\]**

The server name requested by the client; this is used by the server to determine what certificate should be used. **HTTP_REQUEST_PROPERTY_SNI_HOST_MAX_LENGTH** has a value of 255, so this buffer can capture an entire DNS name plus a terminal null.

### -field Flags

Type: **[ULONG](/windows/win32/winprog/windows-data-types)**

Identifies how `http.sys` is using the SNI for this connection; the values of the flags are:

**HTTP_REQUEST_PROPERTY_SNI_FLAG_SNI_USED** (0x1). The SNI value was used as part of identifying the endpoint during the handshake for this request. If an SNI was included in the TLS handshake, but `http.sys` still used an IP endpoint for lookup, then this value won't be set.
**HTTP_REQUEST_PROPERTY_SNI_FLAG_NO_SNI** (0x2). The client didn't include an SNI. If this flag is set, then **HTTP_REQUEST_PROPERTY_SNI_FLAG_SNI_USED** can't be set.

## -remarks

Server name indication (SNI), is a part of the TLS Client Hello where the client requests a specific hostname from a server. Hosts often serve a multitude of domains from a single server, and will regularly have different certificates for different domains, meaning that they need to know the SNI in order to decide which certificate to use for the TLS handshake.

## -see-also
