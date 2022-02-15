---
UID: NE:webservices.__unnamed_enum_42
title: WS_HEADER_TYPE (webservices.h)
description: Identifies a type of header.
helpviewer_keywords: ["WS_ACTION_HEADER","WS_FAULT_TO_HEADER","WS_FROM_HEADER","WS_HEADER_TYPE","WS_HEADER_TYPE enumeration [Web Services for Windows]","WS_MESSAGE_ID_HEADER","WS_RELATES_TO_HEADER","WS_REPLY_TO_HEADER","WS_TO_HEADER","webservices/WS_ACTION_HEADER","webservices/WS_FAULT_TO_HEADER","webservices/WS_FROM_HEADER","webservices/WS_HEADER_TYPE","webservices/WS_MESSAGE_ID_HEADER","webservices/WS_RELATES_TO_HEADER","webservices/WS_REPLY_TO_HEADER","webservices/WS_TO_HEADER","wsw.ws_header_type"]
old-location: wsw\ws_header_type.htm
tech.root: wsw
ms.assetid: 4c9b927d-00c7-41e4-bc29-e84a4c23c162
ms.date: 12/05/2018
ms.keywords: WS_ACTION_HEADER, WS_FAULT_TO_HEADER, WS_FROM_HEADER, WS_HEADER_TYPE, WS_HEADER_TYPE enumeration [Web Services for Windows], WS_MESSAGE_ID_HEADER, WS_RELATES_TO_HEADER, WS_REPLY_TO_HEADER, WS_TO_HEADER, webservices/WS_ACTION_HEADER, webservices/WS_FAULT_TO_HEADER, webservices/WS_FROM_HEADER, webservices/WS_HEADER_TYPE, webservices/WS_MESSAGE_ID_HEADER, webservices/WS_RELATES_TO_HEADER, webservices/WS_REPLY_TO_HEADER, webservices/WS_TO_HEADER, wsw.ws_header_type
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
req.typenames: WS_HEADER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_HEADER_TYPE
 - webservices/WS_HEADER_TYPE
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
 - WS_HEADER_TYPE
---

# WS_HEADER_TYPE enumeration


## -description

Identifies a type of header.

## -enum-fields

### -field WS_ACTION_HEADER:1

The Action addressing header.
                

This header can be used with the following <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>s:
                    <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a>
</li>
</ul>

### -field WS_TO_HEADER:2

The To addressing header.
                

This header can be used with the following <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>s:
                    <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a>
</li>
</ul>

### -field WS_MESSAGE_ID_HEADER:3

The MessageID addressing header.
                

This header can be used with the following <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>s:
                    <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNIQUE_ID_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a>
</li>
</ul>


This header is not supported for <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>.

### -field WS_RELATES_TO_HEADER:4

The RelatesTo addressing header.
                

This header can be used with the following <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a>s:
                    <ul>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_UNIQUE_ID_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_XML_STRING_TYPE</a>
</li>
<li>
<a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_WSZ_TYPE</a>
</li>
</ul>


This header is not supported for <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>.

### -field WS_FROM_HEADER:5

The From addressing header.
                

This header is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ENDPOINT_ADDRESS_TYPE</a>.
                

This header is not supported for <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>.

### -field WS_REPLY_TO_HEADER:6

The ReplyTo addressing header.
                

This header is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ENDPOINT_ADDRESS_TYPE</a>.
                

This header is not supported for <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>.

### -field WS_FAULT_TO_HEADER:7

The FaultTo addressing header, in <a href="/windows/desktop/api/webservices/ns-webservices-ws_endpoint_address">WS_ENDPOINT_ADDRESS</a> format.
                

This header is used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ENDPOINT_ADDRESS_TYPE</a>.
                

This header is not supported for <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_TRANSPORT</a>.
