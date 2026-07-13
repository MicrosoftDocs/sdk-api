---
UID: NE:http._HTTP_REQUEST_PROPERTY
title: HTTP_REQUEST_PROPERTY (http.h)
description: Defines the properties that are configured by the HTTP Server API on a request.
helpviewer_keywords: ["*PHTTP_REQUEST_PROPERTY","*PHTTP_REQUEST_PROPERTY enumeration [HTTP]","HTTP_REQUEST_PROPERTY","HTTP_REQUEST_PROPERTY enumeration [HTTP]","HttpRequestPropertyStreamError","http.http_Request_property","http/*PHTTP_REQUEST_PROPERTY","http/HTTP_REQUEST_PROPERTY","http/HttpRequestPropertyStreamError"]
old-location: http\http_Request_property.htm
tech.root: http
ms.assetid: 02e40197-4e21-4268-8a5e-f9b222f7eba2
ms.date: 09/19/2025
ms.keywords: '*PHTTP_REQUEST_PROPERTY, *PHTTP_REQUEST_PROPERTY enumeration [HTTP], HTTP_REQUEST_PROPERTY, HTTP_REQUEST_PROPERTY enumeration [HTTP], HttpRequestPropertyStreamError, http.http_Request_property, http/*PHTTP_REQUEST_PROPERTY, http/HTTP_REQUEST_PROPERTY, http/HttpRequestPropertyStreamError'
req.header: http.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt:
req.target-min-winversvr:
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
req.typenames: HTTP_REQUEST_PROPERTY, *PHTTP_REQUEST_PROPERTY
req.redist:
ms.custom:
f1_keywords:
 - _HTTP_REQUEST_PROPERTY
 - http/_HTTP_REQUEST_PROPERTY
 - PHTTP_REQUEST_PROPERTY
 - http/PHTTP_REQUEST_PROPERTY
 - HTTP_REQUEST_PROPERTY
 - http/HTTP_REQUEST_PROPERTY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Http.h
api_name:
 - HTTP_REQUEST_PROPERTY
---

## -description

The **HTTP\_REQUEST\_PROPERTY** enumeration defines the properties that you can configured to be queried or set by the HTTP Server API on a request.

## -enum-fields

### -field HttpRequestPropertyIsb

Action: Query.
PVOID Input/Output value: ULONG64

Retrieve the ideal send backlog size for a request (see [SIO_WSK_QUERY_IDEAL_SEND_BACKLOG](/windows-hardware/drivers/network/sio-wsk-query-ideal-send-backlog)).

### -field HttpRequestPropertyTcpInfoV0

Action: Query.
PVOID Input/Output value: [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)

Retrieve the **TCP_INFO_v0** statistics for a request. Uses the *Qualifier* parameter.

### -field HttpRequestPropertyQuicStats

Action: Query.
PVOID Input/Output value: [QUIC_STATISTICS](https://github.com/microsoft/msquic/blob/main/src/inc/msquic.h)

Retrieve the **QUIC_STATISTICS** statistics for a request. Uses the *Qualifier* parameter.

### -field HttpRequestPropertyTcpInfoV1

Action: Query.
PVOID Input/Output value: [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)

Retrieve the **TCP_INFO_v1** statistics for a request. Uses the *Qualifier* parameter.

### -field HttpRequestPropertySni

Action: Query.
PVOID Input/Output value: [HTTP_REQUEST_PROPERTY_SNI](./ns-http-http_request_property_sni.md)

Retrieve the Server Name Indication for the request's TLS connection, in a **HTTP_REQUEST_PROPERTY_SNI**.

### -field HttpRequestPropertyStreamError

Action: Set.
PVOID Input/Output value: [HTTP_REQUEST_PROPERTY_STREAM_ERROR](/windows/win32/api/http/ns-http-http_request_property_stream_error)

Set an (HTTP/2 or HTTP/3) **HTTP_REQUEST_PROPERTY_STREAM_ERROR** struct on a request. The [HTTP\_REQUEST\_PROPERTY\_STREAM\_ERROR](/windows/win32/api/http/ns-http-http_request_property_stream_error) structure contains the configuration data for this property.

### -field HttpRequestPropertyWskApiTimings

Action: Query.
PVOID Input/Output value: [HTTP_WSK_API_TIMINGS](./ns-http-http_wsk_api_timings.md)

Retrieve the **HTTP_WSK_API_TIMINGS** statistics for a request. Only used for non-QUIC requests (HTTP/1.1, HTTP/2). This property requires additional configuration to enable its use; see Remarks.

### -field HttpRequestPropertyQuicApiTimings

Action: Query.
PVOID Input/Output value: HTTP_QUIC_API_TIMINGS

Retrieve the **HTTP_QUIC_API_TIMINGS** statistics for a request. Used only for HTTP/3 requests. This property requires additional configuration to enable its use; see Remarks.

### -field HttpRequestPropertyQuicStatsV2

Action: Query.
PVOID Input/Output value: [QUIC_STATISTICS_V2](https://github.com/microsoft/msquic/blob/main/src/inc/msquic.h)

Retrieve the **QUIC_STATISTICS_V2** statistics for a request. Uses the *Qualifier* parameter.

### -field HttpRequestPropertyQuicStreamStats

Action: Query.
PVOID Input/Output value: [QUIC_STREAM_STATISTICS](https://github.com/microsoft/msquic/blob/main/src/inc/msquic.h)

Retrieve the **QUIC_STREAM_STATISTICS** statistics for a request.

### -field HttpRequestPropertyTcpInfoV2

Action: Query.
PVOID Input/Output value: [TCP_INFO_v2](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v2)

Retrieve extended **TCP_INFO_v2** statistics for a request. Uses the *Qualifier* parameter.

### -field HttpRequestPropertyTlsClientHello

Action: Query.
PVOID Input/Output value: BYTE\[\]

Retrieve the contents of the TLS Client Hello message sent by the client at the start of the connection for that request. This property requires additional configuration to enable its use; see Remarks.

### -field HttpRequestPropertyTransportIdleConnectionTimeout

Action: Set.
PVOID Input/Output value: USHORT

Set a timeout in seconds for if this request goes idle.

### -field HttpRequestPropertyDscpTag

Action: Set.
PVOID Input/Output value: BYTE

Set the differentiated services code point (DSCP) tag to the supplied BYTE value on all packets sent in the response to this request. This is a 6-bit value internally, so the maximum value is 0x3F.

### -field HttpRequestPropertyTlsCipherInfo

Action: Query.
PVOID Input/Output value: [SecPkgContext_CipherInfo](/windows/win32/api/schannel/ns-schannel-secpkgcontext_cipherinfo)

Retrieve the cipher suite and parameters selected for this connection in the TLS handshake.

## -remarks

The **HTTP\_REQUEST\_PROPERTY** enumeration types are used to set or query the configurations on a request. A member of this enumeration together with the associated configuration structure is used by [HttpSetRequestProperty](/windows/win32/api/http/nf-http-httpsetrequestproperty) to define the configuration parameters.

**HttpRequestPropertyWskApiTimings** and **HttpRequestPropertyQuicApiTimings**. These properties require the `HKLM\System\CurrentControlSet\Services\Http\Parameters:EnableExtendedEvents` registry value to be set to 0x1 before starting or restarting the HTTP service.

**HttpRequestPropertyTlsClientHello**. To confirm the availability of this feature, call [HttpIsFeatureSupported](/windows/win32/api/http/nf-http-httpisfeaturesupported) and pass **HttpFeatureCacheTlsClientHello**. Because caching the TLS Client Hello is expensive per-connection, to enable this feature you'll need to call [HttpSetServiceConfiguration](/windows/win32/api/http/nf-http-httpsetserviceconfiguration) with an **HTTP_SERVICE_CONFIG_SSL_SET** struct in *pConfigInformation* with **HTTP_SERVICE_CONFIG_SSL_FLAG_ENABLE_CACHE_CLIENT_HELLO** set (see [HTTP_SERVICE_CONFIG_SSL_PARAM](/windows/win32/api/http/ns-http-http_service_config_ssl_param)). Since a TLS Client Hello doesn't have a fixed length, this property can be queried with a NULL buffer pointer to determine the size of a buffer you need; see the example in [HttpQueryRequestProperty](/windows/win32/http/http/nf-http-httpqueryrequestproperty) for details.

## -see-also

[HttpSetRequestProperty](/windows/win32/api/http/nf-http-httpsetrequestproperty)
