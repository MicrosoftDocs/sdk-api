---
UID: NS:webservices._WS_ENDPOINT_ADDRESS
title: WS_ENDPOINT_ADDRESS (webservices.h)
description: Represents the network address of an endpoint.
helpviewer_keywords: ["WS_ENDPOINT_ADDRESS","WS_ENDPOINT_ADDRESS structure [Web Services for Windows]","webservices/WS_ENDPOINT_ADDRESS","wsw.ws_endpoint_address"]
old-location: wsw\ws_endpoint_address.htm
tech.root: wsw
ms.assetid: 4e9b5f3e-849f-46aa-a94a-3cd6ae16275f
ms.date: 12/05/2018
ms.keywords: WS_ENDPOINT_ADDRESS, WS_ENDPOINT_ADDRESS structure [Web Services for Windows], webservices/WS_ENDPOINT_ADDRESS, wsw.ws_endpoint_address
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
req.typenames: WS_ENDPOINT_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_ENDPOINT_ADDRESS
 - webservices/_WS_ENDPOINT_ADDRESS
 - WS_ENDPOINT_ADDRESS
 - webservices/WS_ENDPOINT_ADDRESS
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
 - WS_ENDPOINT_ADDRESS
---

# WS_ENDPOINT_ADDRESS structure


## -description

Represents the network address of an endpoint.

## -struct-fields

### -field url

The URL portion of the address.  
                

The URL is always in escaped form.  

If this string is zero-length, then
                    the URL is assumed to be the anonymous address.  The anonymous
                    address string is automatically mapped to/from the zero-length string
                    when the endpoint address is serialized or deserialized
                    using <a href="/windows/desktop/api/webservices/ne-webservices-ws_type">WS_ENDPOINT_ADDRESS_TYPE</a>.
                

The value of this field corresponds to the Address element of the 
                    WS-Addressing specifications.

### -field headers

A <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> handle to a set of header elements
                    that represent the reference parameters for the endpoint address.
                

The headers are required to properly interact with the endpoint.
                    They are used to further qualify the address (URL).
                

The headers should be treated as opaque values to the user of
                    the endpoint address.
                

See <a href="/windows/desktop/api/webservices/nf-webservices-wsaddressmessage">WsAddressMessage</a> for information on how to 
                    add the headers to a message being sent.
                

This field may be <b>NULL</b> if there are no headers.
                

This value of this field corresponds to the content of the 
                    ReferenceParameters element of the WS-Addressing specifications.

### -field extensions

A <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> handle to a set of extension elements.
                    Extension elements are used to include additional information within an
                    endpoint address.  This field may be <b>NULL</b> if there are no extension elements.
                

This value of this field corresponds to the other elements
                    defined by WS-Addressing and any extension elements.  The elements must 
                    appear in the correct order according to the specification, followed
                    by extension elements.  This field should not contain elements for Address 
                    or ReferenceParameters, or Identity, since these values are represented directly by 
                    other fields of this structure.
                

If the ReferenceProperties element is present (as defined by
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_addressing_version">WS_ADDRESSING_VERSION_0_9</a>), it must be the first element 
                    within the <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a>.

### -field identity

The security identity of the endpoint represented by this endpoint address.
                

This field corresponds to the Identity element, which is an extension
                    of the base WS-Addressing specifications.

## -remarks

Only the URL field is required (other fields may be <b>NULL</b>).