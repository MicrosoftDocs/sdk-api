---
UID: NE:webservices.WS_SERVICE_ENDPOINT_PROPERTY_ID
title: WS_SERVICE_ENDPOINT_PROPERTY_ID
author: windows-sdk-content
description: Each property represents optional parameters for configuring the given WS_SERVICE_ENDPOINT structure. This enumeration is used within the WS_SERVICE_ENDPOINT_PROPERTY structure that is part of WS_SERVICE_ENDPOINT.
old-location: wsw\ws_service_endpoint_property_id.htm
old-project: wsw
ms.assetid: f6b33fe5-a9e9-4733-8b6c-4b01009d3277
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WS_SERVICE_ENDPOINT_PROPERTY_ACCEPT_CHANNEL_CALLBACK, WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_MAX_SIZE, WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_TRIM_SIZE, WS_SERVICE_ENDPOINT_PROPERTY_CHECK_MUST_UNDERSTAND, WS_SERVICE_ENDPOINT_PROPERTY_CLOSE_CHANNEL_CALLBACK, WS_SERVICE_ENDPOINT_PROPERTY_ID, WS_SERVICE_ENDPOINT_PROPERTY_ID enumeration [Web Services for Windows], WS_SERVICE_ENDPOINT_PROPERTY_LISTENER_PROPERTIES, WS_SERVICE_ENDPOINT_PROPERTY_MAX_ACCEPTING_CHANNELS, WS_SERVICE_ENDPOINT_PROPERTY_MAX_CALL_POOL_SIZE, WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNELS, WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNEL_POOL_SIZE, WS_SERVICE_ENDPOINT_PROPERTY_MAX_CONCURRENCY, WS_SERVICE_ENDPOINT_PROPERTY_MESSAGE_PROPERTIES, WS_SERVICE_ENDPOINT_PROPERTY_METADATA, WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE, WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX, webservices/WS_SERVICE_ENDPOINT_PROPERTY_ACCEPT_CHANNEL_CALLBACK, webservices/WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_MAX_SIZE, webservices/WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_TRIM_SIZE, webservices/WS_SERVICE_ENDPOINT_PROPERTY_CHECK_MUST_UNDERSTAND, webservices/WS_SERVICE_ENDPOINT_PROPERTY_CLOSE_CHANNEL_CALLBACK, webservices/WS_SERVICE_ENDPOINT_PROPERTY_ID, webservices/WS_SERVICE_ENDPOINT_PROPERTY_LISTENER_PROPERTIES, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MAX_ACCEPTING_CHANNELS, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MAX_CALL_POOL_SIZE, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNELS, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNEL_POOL_SIZE, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MAX_CONCURRENCY, webservices/WS_SERVICE_ENDPOINT_PROPERTY_MESSAGE_PROPERTIES, webservices/WS_SERVICE_ENDPOINT_PROPERTY_METADATA, webservices/WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE, webservices/WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX, wsw.ws_service_endpoint_property_id
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WS_SERVICE_ENDPOINT_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SERVICE_ENDPOINT_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SERVICE_ENDPOINT_PROPERTY_ID enumeration


## -description


Each property represents optional parameters for configuring 
                the given <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> structure.
            This enumeration is used within the <a href="https://msdn.microsoft.com/4342d1d2-3126-401b-8019-c7dd243d4ac4">WS_SERVICE_ENDPOINT_PROPERTY</a> structure that is part of <b>WS_SERVICE_ENDPOINT</b>.


## -enum-fields




### -field WS_SERVICE_ENDPOINT_PROPERTY_ACCEPT_CHANNEL_CALLBACK

Used with <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>.
                    The value is a pointer to WS_SERVICE_PROPERTY_ACCEPT_CALLBACK structure. 
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_CLOSE_CHANNEL_CALLBACK

Used with <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>.
                    The value is a pointer to WS_SERVICE_PROPERTY_CLOSE_CALLBACK structure. 
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_MAX_ACCEPTING_CHANNELS

Used with <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>, this specifies the maximum number of concurrent channels service host will have 
                    actively accepting new connections for a given endpoint.                     When not specified this value is set to 1. If an endpoint specifies a default message handler (See <b>WS_SERVICE_ENDPOINT</b>) concurrency 
                    has to be 1. 



### -field WS_SERVICE_ENDPOINT_PROPERTY_MAX_CONCURRENCY

Used with <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>, this specifies the maximum number of concurrent calls that would be serviced on a session based channel.
                    When not specified this value is set to 1. If an endpoint specifies a default message handler (See <b>WS_SERVICE_ENDPOINT</b> concurrency 
                    has to be 1. 
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_MAX_SIZE

Maximum <a href="https://msdn.microsoft.com/library/windows/hardware/dn926854">heap</a> size for body deserialization.
                

This is the heap available setting used for deserializing the body. This heap is also 
                    available to service operations for allocating out parameters.
                

Default is 65535 bytes.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_BODY_HEAP_TRIM_SIZE


<a href="https://msdn.microsoft.com/library/windows/hardware/dn926854">Heap</a> trim size for body deserialization.
                

This is the heap available setting used for deserializing the body. This heap is also 
                    available to service operations for allocating out parameters.
                

Default is 4096 bytes.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_MESSAGE_PROPERTIES

This property allows the user to specify properties of the message
                    objects used by the endpoint to send and receive messages.
                

This property may be specified when the service host is created.
                

The value specified should be of type <a href="https://msdn.microsoft.com/74ad74fd-457a-4408-8032-15d365f98b14">WS_MESSAGE_PROPERTIES</a>.
                

The following message properties may be specified:
                

<ul>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_HEAP_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_XML_READER_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_XML_WRITER_PROPERTIES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7398225c-afbd-45c6-9a32-8b8892f0ff8a">WS_MESSAGE_PROPERTY_MAX_PROCESSED_HEADERS</a>
</li>
</ul>

### -field WS_SERVICE_ENDPOINT_PROPERTY_MAX_CALL_POOL_SIZE

The maximum number of call servicing objects that would be pooled to service a message object, on a given
                    endpoint. Note that in case of session based channels many call objects can be used on a single 
                                        channel if <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_MAX_CONCURRENCY</a> is greater than 1. 


For sessionless channels this property should ideally be equal to <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNEL_POOL_SIZE</a>.
                

Default is 100.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNEL_POOL_SIZE

The maximum number of <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> which will be pooled by Service Host on a given
                    endpoint.
                

Default is 100.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_LISTENER_PROPERTIES

Listener properties.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_CHECK_MUST_UNDERSTAND

Enables or disables must understand header verification on an endpoint. This is 'TRUE' by default.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE

This property can be set to <a href="https://msdn.microsoft.com/35e66c77-db26-4806-9b56-51539b23bb61">WS_METADATA_EXCHANGE_TYPE_MEX</a> to enable 
                    servicing of WS-MetadataExchange requests on the endpoint. In case the application wishes to 
                    expose metadata through HTTP GET, this property can be set to <b>WS_METADATA_EXCHANGE_TYPE_HTTP_GET</b>

If not specified, the default value of this property is '<a href="https://msdn.microsoft.com/35e66c77-db26-4806-9b56-51539b23bb61">WS_METADATA_EXCHANGE_TYPE_NONE</a>'. 
                

Note that this property when set to <a href="https://msdn.microsoft.com/35e66c77-db26-4806-9b56-51539b23bb61">WS_METADATA_EXCHANGE_TYPE_HTTP_GET</a> changes the <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> property 
                    <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a> and
                    <b>WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</b> to <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_PREFIX_PATH</a>. 
                

When setting this property to WS_METADATA_EXCHANGE_TYPE_HTTP_GET an application must not specify <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_EXACT_PATH</a> for the listener 
                    properties <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a> and <b>WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</b>for the given <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_METADATA

Specifies the WSDL port name, binding name and binding namespace for the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">endpoint</a>. 
                

This property must be specified to enable the participation of the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> in WS-Metadata Exchange.
                

See <a href="https://msdn.microsoft.com/e02ea746-ed56-48a7-8cd4-9e51d100ef2a">WS_SERVICE_ENDPOINT_METADATA</a> for more details.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_URL_SUFFIX

Specifies the suffix which is concatenated as is to the <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> URL to generate a URL for WS-MetadataExchange v1.1 requests servicing. 
                    The generated URL is used to compare against the 'to' header of the message received. Note that if the message does not contain a 'to' header the requests is not
                    serviced. 
                

This property must only be specified if <a href="https://msdn.microsoft.com/f6b33fe5-a9e9-4733-8b6c-4b01009d3277">WS_SERVICE_ENDPOINT_PROPERTY_METADATA_EXCHANGE_TYPE</a> is set to <a href="https://msdn.microsoft.com/35e66c77-db26-4806-9b56-51539b23bb61">WS_METADATA_EXCHANGE_TYPE_MEX</a>.
                

Specifying this property is useful in cases where an application wishes to handle WS-Transfer Get requests as well as use the same endpoint to service 
                    WS-MetadataExchange v1.1 requests. The generate URL in this case is used to filter out WS-Transfer Get requests for Ws-MetadataExchange v1.1. 
                

By default no filtering is done for WS-MetadataExchange v1.1 for MEX and all WS-Transfer GET requests will be handled by the endpoint for Ws-MetadataExchange v1.1, if 
                    Ws-MetadataExchange v1.1 is enabled on the endpoint.
                

Note that this property changes the <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> property <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a> and
                    <b>WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</b> to <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_PREFIX_PATH</a>. 
                

When setting this property an application must not specify <a href="https://msdn.microsoft.com/65449a2d-88c3-431e-83d5-ecb182463cf5">WS_MATCH_URL_EXACT_PATH</a> for the listener 
                    properties <a href="https://msdn.microsoft.com/4998d538-628f-4939-9db9-612e882e68b1">WS_LISTENER_PROPERTY_TRANSPORT_URL_MATCHING_OPTIONS</a> and <b>WS_LISTENER_PROPERTY_TO_HEADER_MATCHING_OPTIONS</b> 
                    for the given <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a>.
                


### -field WS_SERVICE_ENDPOINT_PROPERTY_MAX_CHANNELS

The maximum number of channels that can be serviced on the endpoint.
                

The default value is 100.
                

