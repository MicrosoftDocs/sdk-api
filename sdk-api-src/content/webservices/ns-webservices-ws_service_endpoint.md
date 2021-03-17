---
UID: NS:webservices._WS_SERVICE_ENDPOINT
title: WS_SERVICE_ENDPOINT (webservices.h)
description: Represents an individual endpoint on a service host. The properties on the endpoint are used to specify the address, binding and contract.
helpviewer_keywords: ["WS_SERVICE_ENDPOINT","WS_SERVICE_ENDPOINT structure [Web Services for Windows]","webservices/WS_SERVICE_ENDPOINT","wsw.ws_service_endpoint"]
old-location: wsw\ws_service_endpoint.htm
tech.root: wsw
ms.assetid: 6b15fc3f-5e4b-4eb3-b337-0170b0ca746f
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_ENDPOINT, WS_SERVICE_ENDPOINT structure [Web Services for Windows], webservices/WS_SERVICE_ENDPOINT, wsw.ws_service_endpoint
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
req.typenames: WS_SERVICE_ENDPOINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_SERVICE_ENDPOINT
 - webservices/_WS_SERVICE_ENDPOINT
 - WS_SERVICE_ENDPOINT
 - webservices/WS_SERVICE_ENDPOINT
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
 - WS_SERVICE_ENDPOINT
---

# WS_SERVICE_ENDPOINT structure


## -description

Represents an individual endpoint on a service host. The properties on the endpoint
                are used to specify the address, binding and contract.

## -struct-fields

### -field address

The URL address on which the endpoint is going to listen.

### -field channelBinding

The binding for the channel/listener.

### -field channelType

The <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">type of channel</a> being hosted by the endpoint.

### -field securityDescription

A description of the security required for this channel. This can be <b>NULL</b> if no security is required.

### -field contract

The contract of the endpoint.

### -field authorizationCallback

Authorization callback for the service endpoint.

### -field properties

An array of properties to configure the service endpoint.

### -field propertyCount

Number of elements in the WS_SERVICE_ENDPOINT_PROPERTY array.

### -field channelProperties

                    Channel properties associated with the endpoint. An application should be careful in modifying default values. For example, modifying send/receive timeouts may result in unexpected behavior and cause the client to fail.