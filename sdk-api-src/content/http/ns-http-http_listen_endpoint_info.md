---
UID: NS:http._HTTP_LISTEN_ENDPOINT_INFO
title: HTTP_LISTEN_ENDPOINT_INFO (http.h)
description: Controls whether IP-based URLs should listen on the specific IP address or on a wildcard.
helpviewer_keywords: ["*PHTTP_LISTEN_ENDPOINT_INFO","HTTP_LISTEN_ENDPOINT_INFO","HTTP_LISTEN_ENDPOINT_INFO structure [HTTP]","PHTTP_LISTEN_ENDPOINT_INFO","PHTTP_LISTEN_ENDPOINT_INFO structure pointer [HTTP]","http.http_listen_endpoint_info","http/HTTP_LISTEN_ENDPOINT_INFO","http/PHTTP_LISTEN_ENDPOINT_INFO"]
old-location: http\http_listen_endpoint_info.htm
tech.root: http
ms.assetid: ad6553ba-4272-44af-af77-2bf1a4102b60
ms.date: 12/05/2018
ms.keywords: '*PHTTP_LISTEN_ENDPOINT_INFO, HTTP_LISTEN_ENDPOINT_INFO, HTTP_LISTEN_ENDPOINT_INFO structure [HTTP], PHTTP_LISTEN_ENDPOINT_INFO, PHTTP_LISTEN_ENDPOINT_INFO structure pointer [HTTP], http.http_listen_endpoint_info, http/HTTP_LISTEN_ENDPOINT_INFO, http/PHTTP_LISTEN_ENDPOINT_INFO'
req.header: http.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: HTTP_LISTEN_ENDPOINT_INFO, *PHTTP_LISTEN_ENDPOINT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _HTTP_LISTEN_ENDPOINT_INFO
 - http/_HTTP_LISTEN_ENDPOINT_INFO
 - PHTTP_LISTEN_ENDPOINT_INFO
 - http/PHTTP_LISTEN_ENDPOINT_INFO
 - HTTP_LISTEN_ENDPOINT_INFO
 - http/HTTP_LISTEN_ENDPOINT_INFO
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
 - HTTP_LISTEN_ENDPOINT_INFO
---

# HTTP_LISTEN_ENDPOINT_INFO structure


## -description

Controls whether IP-based URLs should listen on the specific IP address or on a wildcard.

## -struct-fields

### -field Flags

The <a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a> structure that specifies if the property is present.

### -field EnableSharing

A Boolean value that specifies whether sharing is enabled.

## -see-also

<a href="/windows/desktop/api/http/ns-http-http_property_flags">HTTP_PROPERTY_FLAGS</a>