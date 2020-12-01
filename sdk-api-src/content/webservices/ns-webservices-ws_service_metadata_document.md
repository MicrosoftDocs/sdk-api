---
UID: NS:webservices._WS_SERVICE_METADATA_DOCUMENT
title: WS_SERVICE_METADATA_DOCUMENT (webservices.h)
description: Specifies the individual documents that make up the service metadata.
helpviewer_keywords: ["WS_SERVICE_METADATA_DOCUMENT","WS_SERVICE_METADATA_DOCUMENT structure [Web Services for Windows]","webservices/WS_SERVICE_METADATA_DOCUMENT","wsw.ws_service_metadata_document"]
old-location: wsw\ws_service_metadata_document.htm
tech.root: wsw
ms.assetid: d15fb735-9f82-4dd2-8586-f67999ab9727
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_METADATA_DOCUMENT, WS_SERVICE_METADATA_DOCUMENT structure [Web Services for Windows], webservices/WS_SERVICE_METADATA_DOCUMENT, wsw.ws_service_metadata_document
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
req.typenames: WS_SERVICE_METADATA_DOCUMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_METADATA_DOCUMENT
 - webservices/_WS_SERVICE_METADATA_DOCUMENT
 - WS_SERVICE_METADATA_DOCUMENT
 - webservices/WS_SERVICE_METADATA_DOCUMENT
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
 - WS_SERVICE_METADATA_DOCUMENT
---

# WS_SERVICE_METADATA_DOCUMENT structure


## -description

Specifies the individual documents that make up the service metadata.

## -struct-fields

### -field content

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a>* representing the specific  XML Schema, WSDL or a Policy document.
                    The service model expects this to be valid for the lifetime of the <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>.

### -field name

The name of the document which will be suffixed to the URL path on which this document is serviced for HTTP GET support
                    for metadata retrieval. Note that this can be set to <b>NULL</b> if the application is only using Ws-MetadataExchange 1.1 for servicing
                    metadata request.
                

See <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_endpoint_property_id">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> service endpoint property to see how to enable HTTP GET support or
                    WS-MetadataExchange 1.1 for servicing metadata request.