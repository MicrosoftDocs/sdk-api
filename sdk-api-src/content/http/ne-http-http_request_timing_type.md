---
UID: NE:http._HTTP_REQUEST_TIMING_TYPE
title: HTTP_REQUEST_TIMING_TYPE
description: Defines constants that specify possible request timings for which information will be returned in [HTTP_REQUEST_TIMING_INFO](/windows/win32/api/http/ns-http-http_request_timing_info).
ms.date: 01/10/2024
tech.root: http
targetos: Windows
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: http.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - http.h
api_name:
 - _HTTP_REQUEST_TIMING_TYPE
 - PHTTP_REQUEST_TIMING_TYPE
 - HTTP_REQUEST_TIMING_TYPE
f1_keywords:
 - _HTTP_REQUEST_TIMING_TYPE
 - http/_HTTP_REQUEST_TIMING_TYPE
 - PHTTP_REQUEST_TIMING_TYPE
 - http/PHTTP_REQUEST_TIMING_TYPE
 - HTTP_REQUEST_TIMING_TYPE
 - http/HTTP_REQUEST_TIMING_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - _HTTP_REQUEST_TIMING_TYPE
---

## -description

Defines constants that specify possible request timings for which information will be returned in [HTTP_REQUEST_TIMING_INFO](/windows/win32/api/http/ns-http-http_request_timing_info). Not all timings apply for every request.

## -enum-fields

### -field HttpRequestTimingTypeConnectionStart

Time the connection started.

### -field HttpRequestTimingTypeDataStart

Time the first HTTP byte is received.

### -field HttpRequestTimingTypeTlsCertificateLoadStart

Time TLS certificate loading starts.

### -field HttpRequestTimingTypeTlsCertificateLoadEnd

Time TLS certificate loading ends.

### -field HttpRequestTimingTypeTlsHandshakeLeg1Start

Time TLS leg one handshake starts.

### -field HttpRequestTimingTypeTlsHandshakeLeg1End

Time TLS leg one handshake ends.

### -field HttpRequestTimingTypeTlsHandshakeLeg2Start

Time TLS leg two handshake starts.

### -field HttpRequestTimingTypeTlsHandshakeLeg2End

Time TLS leg two handshake ends.

### -field HttpRequestTimingTypeTlsAttributesQueryStart

Time TLS attribute query starts.

### -field HttpRequestTimingTypeTlsAttributesQueryEnd

Time TLS attribute query ends.

### -field HttpRequestTimingTypeTlsClientCertQueryStart

Time TLS client certificate query starts.

### -field HttpRequestTimingTypeTlsClientCertQueryEnd

Time TLS client certificate query ends.

### -field HttpRequestTimingTypeHttp2StreamStart

Time HTTP2 streaming starts.

### -field HttpRequestTimingTypeHttp2HeaderDecodeStart

Time HTTP2 header decoding starts.

### -field HttpRequestTimingTypeHttp2HeaderDecodeEnd

Time HTTP2 header decoding ends.

### -field HttpRequestTimingTypeRequestHeaderParseStart

Time HTTP header parsing starts. For most requests, this is a good timestamp to use as a per-request starting timestamp.

### -field HttpRequestTimingTypeRequestHeaderParseEnd

Time HTTP header parsing ends.

### -field HttpRequestTimingTypeRequestRoutingStart

Time `Http.Sys` starts to determine which request queue to route the request to.

### -field HttpRequestTimingTypeRequestRoutingEnd

Time `Http.Sys` has determined which request queue to route the request to.

### -field HttpRequestTimingTypeRequestQueuedForInspection

Time the request is queued for inspection.

### -field HttpRequestTimingTypeRequestDeliveredForInspection

Time the request is delivered for inspection.

### -field HttpRequestTimingTypeRequestReturnedAfterInspection

Time the request has finished being inspected.

### -field HttpRequestTimingTypeRequestQueuedForDelegation

Time the request is queued for delegation.

### -field HttpRequestTimingTypeRequestDeliveredForDelegation

Time the request is delivered for delegation.

### -field HttpRequestTimingTypeRequestReturnedAfterDelegation

Time the request was delegated.

### -field HttpRequestTimingTypeRequestQueuedForIO

Time the request was queued to the final request queue for processing.

### -field HttpRequestTimingTypeRequestDeliveredForIO

Time the request was delivered to the final request queue for processing.

### -field HttpRequestTimingTypeHttp3StreamStart

Time HTTP3 streaming starts.

### -field HttpRequestTimingTypeHttp3HeaderDecodeStart

Time HTTP3 header decoding starts.

### -field HttpRequestTimingTypeHttp3HeaderDecodeEnd

Time HTTP3 header decoding ends.

### -field HttpRequestTimingTypeMax

## -remarks

## -see-also
