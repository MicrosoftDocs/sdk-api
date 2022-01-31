---
UID: NE:winhttp._WINHTTP_REQUEST_STAT_ENTRY
title: WINHTTP_REQUEST_STAT_ENTRY (winhttp.h)
description: The WINHTTP_REQUEST_STAT_ENTRY enumeration lists the available types of request statistics.
helpviewer_keywords: ["WINHTTP_REQUEST_STAT_ENTRY","WINHTTP_REQUEST_STAT_ENTRY enumeration [HTTP]","http.winhttp_request_stat_entry","winhttp/WINHTTP_REQUEST_STAT_ENTRY","WinHttpConnectFailureCount","WinHttpProxyFailureCount","WinHttpTlsHandshakeClientLeg1Size","WinHttpTlsHandshakeServerLeg1Size","WinHttpTlsHandshakeClientLeg2Size","WinHttpTlsHandshakeServerLeg2Size","WinHttpRequestHeadersSize","WinHttpRequestHeadersCompressedSize","WinHttpResponseHeadersSize","WinHttpResponseHeadersCompressedSize","WinHttpResponseBodySize","WinHttpResponseBodyCompressedSize","WinHttpProxyTlsHandshakeClientLeg1Size","WinHttpProxyTlsHandshakeServerLeg1Size","WinHttpProxyTlsHandshakeClientLeg2Size","WinHttpProxyTlsHandshakeServerLeg2Size","WinHttpRequestStatLast","WinHttpRequestStatMax","winhttp/WinHttpConnectFailureCount","winhttp/WinHttpProxyFailureCount","winhttp/WinHttpTlsHandshakeClientLeg1Size","winhttp/WinHttpTlsHandshakeServerLeg1Size","winhttp/WinHttpTlsHandshakeClientLeg2Size","winhttp/WinHttpTlsHandshakeServerLeg2Size","winhttp/WinHttpRequestHeadersSize","winhttp/WinHttpRequestHeadersCompressedSize","winhttp/WinHttpResponseHeadersSize","winhttp/WinHttpResponseHeadersCompressedSize","winhttp/WinHttpResponseBodySize","winhttp/WinHttpResponseBodyCompressedSize","winhttp/WinHttpProxyTlsHandshakeClientLeg1Size","winhttp/WinHttpProxyTlsHandshakeServerLeg1Size","winhttp/WinHttpProxyTlsHandshakeClientLeg2Size","winhttp/WinHttpProxyTlsHandshakeServerLeg2Size","winhttp/WinHttpRequestStatLast","winhttp/WinHttpRequestStatMax"]
tech.root: http
ms.assetid: d9620011-7092-4260-a51f-48d84aebc89b
ms.date: 02/25/2020
ms.keywords: WINHTTP_REQUEST_STAT_ENTRY, WINHTTP_REQUEST_STAT_ENTRY enumeration [HTTP], http.winhttp_request_stat_entry, winhttp/WINHTTP_REQUEST_STAT_ENTRY, WinHttpConnectFailureCount, WinHttpProxyFailureCount, WinHttpTlsHandshakeClientLeg1Size, WinHttpTlsHandshakeServerLeg1Size, WinHttpTlsHandshakeClientLeg2Size, WinHttpTlsHandshakeServerLeg2Size, WinHttpRequestHeadersSize, WinHttpRequestHeadersCompressedSize, WinHttpResponseHeadersSize, WinHttpResponseHeadersCompressedSize, WinHttpResponseBodySize, WinHttpResponseBodyCompressedSize, WinHttpProxyTlsHandshakeClientLeg1Size, WinHttpProxyTlsHandshakeServerLeg1Size, WinHttpProxyTlsHandshakeClientLeg2Size, WinHttpProxyTlsHandshakeServerLeg2Size, WinHttpRequestStatLast, WinHttpRequestStatMax, winhttp/WinHttpConnectFailureCount, winhttp/WinHttpProxyFailureCount, winhttp/WinHttpTlsHandshakeClientLeg1Size, winhttp/WinHttpTlsHandshakeServerLeg1Size, winhttp/WinHttpTlsHandshakeClientLeg2Size, winhttp/WinHttpTlsHandshakeServerLeg2Size, winhttp/WinHttpRequestHeadersSize, winhttp/WinHttpRequestHeadersCompressedSize, winhttp/WinHttpResponseHeadersSize, winhttp/WinHttpResponseHeadersCompressedSize, winhttp/WinHttpResponseBodySize, winhttp/WinHttpResponseBodyCompressedSize, winhttp/WinHttpProxyTlsHandshakeClientLeg1Size, winhttp/WinHttpProxyTlsHandshakeServerLeg1Size, winhttp/WinHttpProxyTlsHandshakeClientLeg2Size, winhttp/WinHttpProxyTlsHandshakeServerLeg2Size, winhttp/WinHttpRequestStatLast, winhttp/WinHttpRequestStatMax
req.header: winhttp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1903 [desktop apps only]
req.target-min-winversvr: Windows Server 2019 [desktop apps only]
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
req.typenames: WINHTTP_REQUEST_STAT_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WINHTTP_REQUEST_STAT_ENTRY
 - winhttp/_WINHTTP_REQUEST_STAT_ENTRY
 - WINHTTP_REQUEST_STAT_ENTRY
 - winhttp/WINHTTP_REQUEST_STAT_ENTRY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winhttp.h
api_name:
 - WINHTTP_REQUEST_STAT_ENTRY
---

# WINHTTP_REQUEST_STAT_ENTRY enumeration


## -description

The **WINHTTP\_REQUEST\_STAT\_ENTRY** enumeration lists the available types of request statistics.

## -enum-fields

### -field WinHttpConnectFailureCount:0

The number of connection failures during connection establishment.

### -field WinHttpProxyFailureCount

The number of proxy connection failures during connection establishment.

### -field WinHttpTlsHandshakeClientLeg1Size

The size of the client data for the first leg of the TLS handshake.

### -field WinHttpTlsHandshakeServerLeg1Size

The size of the server data for the first leg of the TLS handshake.

### -field WinHttpTlsHandshakeClientLeg2Size

The size of the client data for the second leg of the TLS handshake.

### -field WinHttpTlsHandshakeServerLeg2Size

The size of the server data for the second leg of the TLS handshake.

### -field WinHttpRequestHeadersSize

The size of the request headers.

### -field WinHttpRequestHeadersCompressedSize

The compressed size of the request headers.

### -field WinHttpResponseHeadersSize

The size of the response headers.

### -field WinHttpResponseHeadersCompressedSize

The compressed size of the response headers.

### -field WinHttpResponseBodySize

The size of the response body.

### -field WinHttpResponseBodyCompressedSize

The compressed size of the response body.

### -field WinHttpProxyTlsHandshakeClientLeg1Size

The size of the client data for the first leg of the proxy TLS handshake.

### -field WinHttpProxyTlsHandshakeServerLeg1Size

The size of the server data for the first leg of the proxy TLS handshake.

### -field WinHttpProxyTlsHandshakeClientLeg2Size

The size of the client data for the second leg of the proxy TLS handshake.

### -field WinHttpProxyTlsHandshakeServerLeg2Size

The size of the server data for the second leg of the proxy TLS handshake.

### -field WinHttpRequestStatLast

Marker for the end of the list of available statistics.

### -field WinHttpRequestStatMax:32

The maximum number of statistics available.

## -remarks

This structure is used with [WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption) to retrieve statistics for a request by specifying the **WINHTTP\_OPTION\_REQUEST\_STATS** flag.

## -see-also

[WinHttpQueryOption](/windows/desktop/api/winhttp/nf-winhttp-winhttpqueryoption)

[WINHTTP\_REQUEST\_STATS](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)

