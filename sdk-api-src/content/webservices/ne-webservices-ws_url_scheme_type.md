---
UID: NE:webservices.__unnamed_enum_100
title: WS_URL_SCHEME_TYPE (webservices.h)
description: The set of schemes used with WsDecodeUrl, WsEncodeUrl, and WsCombineUrl.
helpviewer_keywords: ["WS_URL_HTTPS_SCHEME_TYPE","WS_URL_HTTP_SCHEME_TYPE","WS_URL_NETPIPE_SCHEME_TYPE","WS_URL_NETTCP_SCHEME_TYPE","WS_URL_SCHEME_TYPE","WS_URL_SCHEME_TYPE enumeration [Web Services for Windows]","WS_URL_SOAPUDP_SCHEME_TYPE","webservices/WS_URL_HTTPS_SCHEME_TYPE","webservices/WS_URL_HTTP_SCHEME_TYPE","webservices/WS_URL_NETPIPE_SCHEME_TYPE","webservices/WS_URL_NETTCP_SCHEME_TYPE","webservices/WS_URL_SCHEME_TYPE","webservices/WS_URL_SOAPUDP_SCHEME_TYPE","wsw.ws_url_scheme_type"]
old-location: wsw\ws_url_scheme_type.htm
tech.root: wsw
ms.assetid: e8763719-6ba0-4e5e-bb71-625d36a45eaf
ms.date: 12/05/2018
ms.keywords: WS_URL_HTTPS_SCHEME_TYPE, WS_URL_HTTP_SCHEME_TYPE, WS_URL_NETPIPE_SCHEME_TYPE, WS_URL_NETTCP_SCHEME_TYPE, WS_URL_SCHEME_TYPE, WS_URL_SCHEME_TYPE enumeration [Web Services for Windows], WS_URL_SOAPUDP_SCHEME_TYPE, webservices/WS_URL_HTTPS_SCHEME_TYPE, webservices/WS_URL_HTTP_SCHEME_TYPE, webservices/WS_URL_NETPIPE_SCHEME_TYPE, webservices/WS_URL_NETTCP_SCHEME_TYPE, webservices/WS_URL_SCHEME_TYPE, webservices/WS_URL_SOAPUDP_SCHEME_TYPE, wsw.ws_url_scheme_type
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_URL_SCHEME_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_URL_SCHEME_TYPE
 - webservices/WS_URL_SCHEME_TYPE
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
 - WS_URL_SCHEME_TYPE
---

# WS_URL_SCHEME_TYPE enumeration


## -description

The set of schemes used with <a href="/windows/desktop/api/webservices/nf-webservices-wsdecodeurl">WsDecodeUrl</a>, <a href="/windows/desktop/api/webservices/nf-webservices-wsencodeurl">WsEncodeUrl</a>, 
                and <a href="/windows/desktop/api/webservices/nf-webservices-wscombineurl">WsCombineUrl</a>.

## -enum-fields

### -field WS_URL_HTTP_SCHEME_TYPE:0

Denotes the "http" scheme: <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_url">WS_HTTP_URL</a>

### -field WS_URL_HTTPS_SCHEME_TYPE:1

Denotes the "https" scheme: <a href="/windows/desktop/api/webservices/ns-webservices-ws_https_url">WS_HTTPS_URL</a>

### -field WS_URL_NETTCP_SCHEME_TYPE:2

Denotes the "net.tcp" scheme: <a href="/windows/desktop/api/webservices/ns-webservices-ws_nettcp_url">WS_NETTCP_URL</a>

### -field WS_URL_SOAPUDP_SCHEME_TYPE:3

Denotes the "soap.udp" scheme: <a href="/windows/desktop/api/webservices/ns-webservices-ws_soapudp_url">WS_SOAPUDP_URL</a>

### -field WS_URL_NETPIPE_SCHEME_TYPE:4

Windows 8 or later: Denotes the "net.pipe" scheme: <a href="/windows/win32/api/webservices/ns-webservices-ws_netpipe_url">WS_NETPIPE_URL</a>
