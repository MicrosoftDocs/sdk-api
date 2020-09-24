---
UID: NS:webservices._WS_HTTP_URL
title: WS_HTTP_URL (webservices.h)
description: The URL subtype for specifying an HTTP URL.
helpviewer_keywords: ["WS_HTTP_URL","WS_HTTP_URL structure [Web Services for Windows]","webservices/WS_HTTP_URL","wsw.ws_http_url"]
old-location: wsw\ws_http_url.htm
tech.root: wsw
ms.assetid: 36f4dda6-d46a-44cd-b4cd-597fa3298870
ms.date: 12/05/2018
ms.keywords: WS_HTTP_URL, WS_HTTP_URL structure [Web Services for Windows], webservices/WS_HTTP_URL, wsw.ws_http_url
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
req.typenames: WS_HTTP_URL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HTTP_URL
 - webservices/_WS_HTTP_URL
 - WS_HTTP_URL
 - webservices/WS_HTTP_URL
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
 - WS_HTTP_URL
---

# WS_HTTP_URL structure


## -description

The URL subtype for specifying an HTTP URL.

## -struct-fields

### -field url

The base type from which this URL subtype and all other URL subtypes derive. The <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> is <b>WS_URL_HTTP_SCHEME_TYPE</b>.

### -field host

The host name.

### -field port

The port number.

### -field portAsString

The port number as string.

### -field path

The path.

### -field query

The query.

### -field fragment

The fragment.

## -remarks

If used with the <a href="/windows/desktop/api/webservices/nf-webservices-wsdecodeurl">WsDecodeUrl</a> field, portAsString is a zero-length string if no port is specified in url.

## -see-also

<a href="/windows/desktop/api/webservices/ns-webservices-ws_https_url">WS_HTTPS_URL</a>



<a href="/windows/desktop/api/webservices/ns-webservices-ws_nettcp_url">WS_NETTCP_URL</a>



<a href="/windows/desktop/api/webservices/ns-webservices-ws_soapudp_url">WS_SOAPUDP_URL</a>