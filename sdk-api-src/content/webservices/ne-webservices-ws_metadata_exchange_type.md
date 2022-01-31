---
UID: NE:webservices.__unnamed_enum_93
title: WS_METADATA_EXCHANGE_TYPE (webservices.h)
description: Information about enabling and disabling types of metadata exchange.
helpviewer_keywords: ["WS_METADATA_EXCHANGE_TYPE","WS_METADATA_EXCHANGE_TYPE enumeration [Web Services for Windows]","WS_METADATA_EXCHANGE_TYPE_HTTP_GET","WS_METADATA_EXCHANGE_TYPE_MEX","WS_METADATA_EXCHANGE_TYPE_NONE","webservices/WS_METADATA_EXCHANGE_TYPE","webservices/WS_METADATA_EXCHANGE_TYPE_HTTP_GET","webservices/WS_METADATA_EXCHANGE_TYPE_MEX","webservices/WS_METADATA_EXCHANGE_TYPE_NONE","wsw.ws_metadata_exchange_type"]
old-location: wsw\ws_metadata_exchange_type.htm
tech.root: wsw
ms.assetid: 35e66c77-db26-4806-9b56-51539b23bb61
ms.date: 12/05/2018
ms.keywords: WS_METADATA_EXCHANGE_TYPE, WS_METADATA_EXCHANGE_TYPE enumeration [Web Services for Windows], WS_METADATA_EXCHANGE_TYPE_HTTP_GET, WS_METADATA_EXCHANGE_TYPE_MEX, WS_METADATA_EXCHANGE_TYPE_NONE, webservices/WS_METADATA_EXCHANGE_TYPE, webservices/WS_METADATA_EXCHANGE_TYPE_HTTP_GET, webservices/WS_METADATA_EXCHANGE_TYPE_MEX, webservices/WS_METADATA_EXCHANGE_TYPE_NONE, wsw.ws_metadata_exchange_type
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
req.typenames: WS_METADATA_EXCHANGE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_METADATA_EXCHANGE_TYPE
 - webservices/WS_METADATA_EXCHANGE_TYPE
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
 - WS_METADATA_EXCHANGE_TYPE
---

## -description

Information about enabling and disabling types of metadata exchange.

## -enum-fields

### -field WS_METADATA_EXCHANGE_TYPE_NONE:0

Disables WS-MetadataExchange/HTTP GET servicing on the <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_endpoint">endpoint</a>.  
                    This is the default value of  <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_endpoint_property_id">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> property.

### -field WS_METADATA_EXCHANGE_TYPE_MEX:1

Enables servicing of WS-MetadataExchange 1.1 request servicing on the <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_endpoint">endpoint</a>.

### -field WS_METADATA_EXCHANGE_TYPE_HTTP_GET:2

Enables servicing of HTTP GET request servicing on the <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_endpoint">endpoint</a> for metadata 
                    retrieval.
