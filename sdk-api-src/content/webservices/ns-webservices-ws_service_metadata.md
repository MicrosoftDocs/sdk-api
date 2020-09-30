---
UID: NS:webservices._WS_SERVICE_METADATA
title: WS_SERVICE_METADATA (webservices.h)
description: Specifies the service metadata documents array. This can be a collection of WSDL/XSD documents represented as an array of WS_STRING.
helpviewer_keywords: ["WS_SERVICE_METADATA","WS_SERVICE_METADATA structure [Web Services for Windows]","webservices/WS_SERVICE_METADATA","wsw.ws_service_metadata"]
old-location: wsw\ws_service_metadata.htm
tech.root: wsw
ms.assetid: f695867d-989d-41a9-ab6e-612a6ef4fb14
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_METADATA, WS_SERVICE_METADATA structure [Web Services for Windows], webservices/WS_SERVICE_METADATA, wsw.ws_service_metadata
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
req.typenames: WS_SERVICE_METADATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_METADATA
 - webservices/_WS_SERVICE_METADATA
 - WS_SERVICE_METADATA
 - webservices/WS_SERVICE_METADATA
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
 - WS_SERVICE_METADATA
---

# WS_SERVICE_METADATA structure


## -description

Specifies the service metadata documents array. This can be a collection of 
                WSDL/XSD documents represented as an array of WS_STRING.

## -struct-fields

### -field documentCount

The count of metadata documents being specified.

### -field documents

A <a href="/windows/win32/api/webservices/ns-webservices-ws_service_metadata_document">WS_SERVICE_METADATA_DOCUMENT</a>* array where element represents a WS_SERVICE_METADATA_DOCUMENT for each individual XML Schema, WSDL or a Policy document. 
                The service model expects this to be valid for the lifetime of the <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>.

### -field serviceName

Reference to WS_XML_STRING representing the name of the service in the WSDL document. Note that this field must be specified along with the serviceNs field. The service model expects this to be valid for the lifetime 
                    of the <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>.

### -field serviceNs

Reference to WS_XML_STRING representing the namespace of the service in the WSDL document. Note that this field must be specified along with the serviceName field.
                The service model expects this to be valid for the lifetime of the <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>.