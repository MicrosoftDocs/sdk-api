---
UID: NS:webservices._WS_SOAPUDP_URL
title: WS_SOAPUDP_URL (webservices.h)
description: The URL subtype for specifying a soap.udp URL.
helpviewer_keywords: ["WS_SOAPUDP_URL","WS_SOAPUDP_URL structure [Web Services for Windows]","webservices/WS_SOAPUDP_URL","wsw.ws_soapudp_url"]
old-location: wsw\ws_soapudp_url.htm
tech.root: wsw
ms.assetid: f39c551f-891b-48c2-8143-84845506cde9
ms.date: 12/05/2018
ms.keywords: WS_SOAPUDP_URL, WS_SOAPUDP_URL structure [Web Services for Windows], webservices/WS_SOAPUDP_URL, wsw.ws_soapudp_url
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
req.typenames: WS_SOAPUDP_URL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SOAPUDP_URL
 - webservices/_WS_SOAPUDP_URL
 - WS_SOAPUDP_URL
 - webservices/WS_SOAPUDP_URL
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
 - WS_SOAPUDP_URL
---

# WS_SOAPUDP_URL structure


## -description

The URL subtype for specifying a soap.udp URL.

## -struct-fields

### -field url

The base type from which this URL subtype and all other URL subtypes derive. The <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> is <b>WS_URL_SOAPUDP_SCHEME_TYPE</b>.

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



<a href="/windows/desktop/api/webservices/ns-webservices-ws_http_url">WS_HTTP_URL</a>



<a href="/windows/desktop/api/webservices/ns-webservices-ws_nettcp_url">WS_NETTCP_URL</a>