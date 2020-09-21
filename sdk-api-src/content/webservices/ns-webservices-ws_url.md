---
UID: NS:webservices._WS_URL
title: WS_URL (webservices.h)
description: The abstract base type for all URL schemes used with WsDecodeUrl and WsEncodeUrl APIs.
helpviewer_keywords: ["WS_URL","WS_URL structure [Web Services for Windows]","webservices/WS_URL","wsw.ws_url"]
old-location: wsw\ws_url.htm
tech.root: wsw
ms.assetid: efc67b64-cedf-4cd9-83b3-047f6c38c6ea
ms.date: 12/05/2018
ms.keywords: WS_URL, WS_URL structure [Web Services for Windows], webservices/WS_URL, wsw.ws_url
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
req.typenames: WS_URL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_URL
 - webservices/_WS_URL
 - WS_URL
 - webservices/WS_URL
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
 - WS_URL
---

# WS_URL structure


## -description

The abstract base type for all URL schemes used with <a href="/windows/desktop/api/webservices/nf-webservices-wsdecodeurl">WsDecodeUrl</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wsencodeurl">WsEncodeUrl</a> APIs.

## -struct-fields

### -field scheme

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_url_scheme_type">WS_URL_SCHEME_TYPE</a> structure that describes the type of URL scheme.