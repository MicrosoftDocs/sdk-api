---
UID: NE:webservices.__unnamed_enum_94
title: WS_SERVICE_PROPERTY_ID (webservices.h)
description: The optional parameters for configuring the service host. This enumeration is used within the WS_SERVICE_PROPERTY structure when calling WsCreateServiceHost or by itself when calling WsGetServiceHostProperty.
helpviewer_keywords: ["WS_SERVICE_PROPERTY_CLOSE_TIMEOUT","WS_SERVICE_PROPERTY_FAULT_DISCLOSURE","WS_SERVICE_PROPERTY_FAULT_LANGID","WS_SERVICE_PROPERTY_HOST_STATE","WS_SERVICE_PROPERTY_HOST_USER_STATE","WS_SERVICE_PROPERTY_ID","WS_SERVICE_PROPERTY_ID enumeration [Web Services for Windows]","WS_SERVICE_PROPERTY_METADATA","webservices/WS_SERVICE_PROPERTY_CLOSE_TIMEOUT","webservices/WS_SERVICE_PROPERTY_FAULT_DISCLOSURE","webservices/WS_SERVICE_PROPERTY_FAULT_LANGID","webservices/WS_SERVICE_PROPERTY_HOST_STATE","webservices/WS_SERVICE_PROPERTY_HOST_USER_STATE","webservices/WS_SERVICE_PROPERTY_ID","webservices/WS_SERVICE_PROPERTY_METADATA","wsw.ws_service_property_id"]
old-location: wsw\ws_service_property_id.htm
tech.root: wsw
ms.assetid: 305fe7ad-e4a2-499a-b34b-e5b7cde53e22
ms.date: 12/05/2018
ms.keywords: WS_SERVICE_PROPERTY_CLOSE_TIMEOUT, WS_SERVICE_PROPERTY_FAULT_DISCLOSURE, WS_SERVICE_PROPERTY_FAULT_LANGID, WS_SERVICE_PROPERTY_HOST_STATE, WS_SERVICE_PROPERTY_HOST_USER_STATE, WS_SERVICE_PROPERTY_ID, WS_SERVICE_PROPERTY_ID enumeration [Web Services for Windows], WS_SERVICE_PROPERTY_METADATA, webservices/WS_SERVICE_PROPERTY_CLOSE_TIMEOUT, webservices/WS_SERVICE_PROPERTY_FAULT_DISCLOSURE, webservices/WS_SERVICE_PROPERTY_FAULT_LANGID, webservices/WS_SERVICE_PROPERTY_HOST_STATE, webservices/WS_SERVICE_PROPERTY_HOST_USER_STATE, webservices/WS_SERVICE_PROPERTY_ID, webservices/WS_SERVICE_PROPERTY_METADATA, wsw.ws_service_property_id
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
req.typenames: WS_SERVICE_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SERVICE_PROPERTY_ID
 - webservices/WS_SERVICE_PROPERTY_ID
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
 - WS_SERVICE_PROPERTY_ID
---

# WS_SERVICE_PROPERTY_ID enumeration


## -description

The optional parameters for configuring the service host.
            This enumeration is used within the <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_property">WS_SERVICE_PROPERTY</a> structure when calling <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a> or by itself when calling <a href="/windows/desktop/api/webservices/nf-webservices-wsgetservicehostproperty">WsGetServiceHostProperty</a>.

## -enum-fields

### -field WS_SERVICE_PROPERTY_HOST_USER_STATE:0

A void pointer
                    used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a>. This property 
                    is made available to different callbacks and service operations as part of the  <a href="/windows/desktop/wsw/ws-operation-context">WS_OPERATION_CONTEXT</a> structure

### -field WS_SERVICE_PROPERTY_FAULT_DISCLOSURE:1

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_fault_disclosure">WS_FAULT_DISCLOSURE</a> value used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a>.
                    This property is used to specify the disclosure level of the error object when its converted into a fault. The default is <b>WS_MINIMAL_FAULT_DISCLOSURE</b>.

### -field WS_SERVICE_PROPERTY_FAULT_LANGID:2

A LANGID used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetservicehostproperty">WsGetServiceHostProperty</a> to create a fault. If none is specified, the default user locale will be used.

### -field WS_SERVICE_PROPERTY_HOST_STATE:3

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_service_host_state">WS_SERVICE_HOST_STATE</a> value  used with <a href="/windows/desktop/api/webservices/nf-webservices-wsgetservicehostproperty">WsGetServiceHostProperty</a> that specifies the current state of the service host.
                

The returned value is a snapshot of the current state, so it is
                    possible that the state may have changed before the caller has
                    had a chance to examine the value.

### -field WS_SERVICE_PROPERTY_METADATA:4

A <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_metadata">WS_SERVICE_METADATA</a> structure used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a> that contains the collection of metadata documents used for WS-MetadataExchange by the <a href="/windows/desktop/wsw/ws-service-host">WS_SERVICE_HOST</a>.

The service name and namespace are used to create a service element inside the WSDL document. The document is identified by means of the service namespace provided as part of <a href="/windows/desktop/api/webservices/ns-webservices-ws_service_metadata">WS_SERVICE_METADATA</a> structure.

 
Note that if a service section is already defined in any of the provided WSDL documents, a service element will not be added on behalf of the application by the runtime.

### -field WS_SERVICE_PROPERTY_CLOSE_TIMEOUT:5

A <b>ULONG</b> used with <a href="/windows/desktop/api/webservices/nf-webservices-wscreateservicehost">WsCreateServiceHost</a> that specifies the maximum amount of time a service model will wait after <a href="/windows/desktop/api/webservices/nf-webservices-wscloseservicehost">WsCloseServiceHost</a> is called. Once the timeout expires service host will abort itself. 
The default is 5 seconds specified in milliseconds as 5000.
