---
UID: NS:webservices._WS_METADATA_ENDPOINT
title: WS_METADATA_ENDPOINT (webservices.h)
description: Information about a single endpoint that was read from metadata documents.
helpviewer_keywords: ["WS_METADATA_ENDPOINT","WS_METADATA_ENDPOINT structure [Web Services for Windows]","webservices/WS_METADATA_ENDPOINT","wsw.ws_metadata_endpoint"]
old-location: wsw\ws_metadata_endpoint.htm
tech.root: wsw
ms.assetid: ce2a45a8-c2e6-4867-b8f1-dcc4f137ef94
ms.date: 12/05/2018
ms.keywords: WS_METADATA_ENDPOINT, WS_METADATA_ENDPOINT structure [Web Services for Windows], webservices/WS_METADATA_ENDPOINT, wsw.ws_metadata_endpoint
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
req.typenames: WS_METADATA_ENDPOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_METADATA_ENDPOINT
 - webservices/_WS_METADATA_ENDPOINT
 - WS_METADATA_ENDPOINT
 - webservices/WS_METADATA_ENDPOINT
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
 - WS_METADATA_ENDPOINT
---

# WS_METADATA_ENDPOINT structure


## -description

Information about a single endpoint that was
                read from metadata documents.

## -struct-fields

### -field endpointAddress

The address of the endpoint.

### -field endpointPolicy

An opaque handle representing the policy of the endpoint.  
                    This handle is good until the metadata object
                    is freed or reset.

### -field portName

The WSDL port name of the endpoint, if available.

### -field serviceName

The WSDL service name of the endpoint, if available.

### -field serviceNs

The WSDL service namespace of the endpoint, if available.

### -field bindingName

The WSDL binding name of the endpoint, if available.

### -field bindingNs

The WSDL binding namespace of the endpoint, if available.

### -field portTypeName

The WSDL portType name of the endpoint, if available.

### -field portTypeNs

The WSDL portType namespace of the endpoint, if available.

