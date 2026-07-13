---
UID: NS:webservices._WS_HTTP_MESSAGE_MAPPING
title: WS_HTTP_MESSAGE_MAPPING (webservices.h)
description: How an HTTP request or response should be represented in a message object.
helpviewer_keywords: ["WS_HTTP_MESSAGE_MAPPING","WS_HTTP_MESSAGE_MAPPING structure [Web Services for Windows]","webservices/WS_HTTP_MESSAGE_MAPPING","wsw.ws_http_message_mapping"]
old-location: wsw\ws_http_message_mapping.htm
tech.root: wsw
ms.assetid: dff8217e-769d-4f0b-acf2-02d6e43589cf
ms.date: 12/05/2018
ms.keywords: WS_HTTP_MESSAGE_MAPPING, WS_HTTP_MESSAGE_MAPPING structure [Web Services for Windows], webservices/WS_HTTP_MESSAGE_MAPPING, wsw.ws_http_message_mapping
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
req.typenames: WS_HTTP_MESSAGE_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_HTTP_MESSAGE_MAPPING
 - webservices/_WS_HTTP_MESSAGE_MAPPING
 - WS_HTTP_MESSAGE_MAPPING
 - webservices/WS_HTTP_MESSAGE_MAPPING
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
 - WS_HTTP_MESSAGE_MAPPING
---

# WS_HTTP_MESSAGE_MAPPING structure


## -description

Specifies information about how an HTTP request or response should be
                represented in a message object.

## -struct-fields

### -field requestMappingOptions

Options that control how information in the HTTP request is mapped to the message object.

### -field responseMappingOptions

Options that control how information in the HTTP response is mapped to the message object.

### -field requestHeaderMappings

An array of pointers to mappings which describe which
                    HTTP headers are mapped to/from headers in the message object
                    for an HTTP request.  The pointers in the array may not be <b>NULL</b>.

### -field requestHeaderMappingCount

The number of items in the requestHeaderMappings array.

### -field responseHeaderMappings

An array of pointers to mappings which describe which
                    HTTP headers are mapped to/from headers in the message object
                    for an HTTP response.  The pointers in the array may not be <b>NULL</b>.

### -field responseHeaderMappingCount

The number of items in the responseHeaderMappings array.

## -remarks

A message may contain additional transport-specific information that is
                not part of the message envelope.  This transport-specific information
                can be exposed programmatically as headers of the message object.  
                These headers are referred to as mapped headers.
            

Each mapped header is stored as regular header element
                in the headers of the message (see <a href="/windows/desktop/api/webservices/ne-webservices-ws_message_property_id">WS_MESSAGE_PROPERTY_HEADER_BUFFER</a>).
                The empty XML namespace ("") is used for mapped headers.
            

This structure specifies how the mapping occurs between an HTTP request
                or response and the mapped headers of the message object.  The structure
                can be specified using the <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_property_id">WS_CHANNEL_PROPERTY_HTTP_MESSAGE_MAPPING</a> property.
            

The following diagram shows how HTTP headers are mapped into
                the headers of a message.
            
:::image type="content" source="images/MappedHeaders.png" border="false" alt-text="Diagram showing a Message object with the MyHeader element highlighted and an arrow pointing to the MyHeader line in an HTTP Request.":::

When a message is received, the HTTP channel
                will automatically copy the specified HTTP headers from the request
                or response to the headers of the message object.  The application
                can then use <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmappedheader">WsGetMappedHeader</a> to get the values of
                the mapped headers.
            

Before a message is sent, an application can add mapped headers
                to the message object using <a href="/windows/desktop/api/webservices/nf-webservices-wsaddmappedheader">WsAddMappedHeader</a>.
                When the message is sent, the HTTP channel will automatically
                remove the specified headers from the headers of message object (so they
                do not appear inside the envelope), and add them as HTTP
                request or response headers.
            

The HTTP channel will only perform this mapping for HTTP headers
                that have been specified in the requestHeaderMappings or
                responseHeaderMappings fields.  The <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_mapping">WS_HTTP_HEADER_MAPPING</a> is used to specify each header, and includes instructions about how
                the message header is transformed to/from an HTTP header.
            

Other information in an HTTP request or response that does not correspond
                to HTTP headers can be mapped into header of the message object by setting the 
                requestMappingOptions or responseMappingOptions.  These mapped values can then be
                extracted using <a href="/windows/desktop/api/webservices/nf-webservices-wsgetmappedheader">WsGetMappedHeader</a>.  
                See <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_writer_property_id">WS_HTTP_REQUEST_MAPPING_OPTIONS</a> or <a href="/windows/win32/api/webservices/ne-webservices-ws_xml_canonicalization_property_id">WS_HTTP_RESPONSE_MAPPING_OPTIONS</a> 
                for information about what information can be mapped into message headers.