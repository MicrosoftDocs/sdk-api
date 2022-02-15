---
UID: NE:webservices.__unnamed_enum_32
title: WS_FAULT_ERROR_PROPERTY_ID (webservices.h)
description: Information about a fault.
helpviewer_keywords: ["WS_FAULT_ERROR_PROPERTY_ACTION","WS_FAULT_ERROR_PROPERTY_FAULT","WS_FAULT_ERROR_PROPERTY_HEADER","WS_FAULT_ERROR_PROPERTY_ID","WS_FAULT_ERROR_PROPERTY_ID enumeration [Web Services for Windows]","webservices/WS_FAULT_ERROR_PROPERTY_ACTION","webservices/WS_FAULT_ERROR_PROPERTY_FAULT","webservices/WS_FAULT_ERROR_PROPERTY_HEADER","webservices/WS_FAULT_ERROR_PROPERTY_ID","wsw.ws_fault_error_property_id"]
old-location: wsw\ws_fault_error_property_id.htm
tech.root: wsw
ms.assetid: f5ae9ee9-18de-428d-9367-aa4a554577ea
ms.date: 12/05/2018
ms.keywords: WS_FAULT_ERROR_PROPERTY_ACTION, WS_FAULT_ERROR_PROPERTY_FAULT, WS_FAULT_ERROR_PROPERTY_HEADER, WS_FAULT_ERROR_PROPERTY_ID, WS_FAULT_ERROR_PROPERTY_ID enumeration [Web Services for Windows], webservices/WS_FAULT_ERROR_PROPERTY_ACTION, webservices/WS_FAULT_ERROR_PROPERTY_FAULT, webservices/WS_FAULT_ERROR_PROPERTY_HEADER, webservices/WS_FAULT_ERROR_PROPERTY_ID, wsw.ws_fault_error_property_id
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
req.typenames: WS_FAULT_ERROR_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_FAULT_ERROR_PROPERTY_ID
 - webservices/WS_FAULT_ERROR_PROPERTY_ID
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
 - WS_FAULT_ERROR_PROPERTY_ID
---

# WS_FAULT_ERROR_PROPERTY_ID enumeration


## -description

Information about a fault.

## -enum-fields

### -field WS_FAULT_ERROR_PROPERTY_FAULT:0

An optional <a href="/windows/desktop/api/webservices/ns-webservices-ws_fault">WS_FAULT</a> value that is the fault representation of the error.  If no
                    fault representation is present, then the value is <b>NULL</b>.
                

To set the WS_FAULT value, pass a WS_FAULT* to <a href="/windows/desktop/api/webservices/nf-webservices-wssetfaulterrorproperty">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the WS_FAULT.  The error object will also
                    add the fault string of the fault to the set of error strings in the error object
                    if the language of the fault string matches that of the error object.
                

To get the WS_FAULT value, pass a WS_FAULT** to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetfaulterrorproperty">WsGetFaultErrorProperty</a>, 
                    which will either return <b>NULL</b> (indicating no fault has been set), or will 
                    return a non-<b>NULL</b> pointer to the WS_FAULT.  The non-<b>NULL</b> pointer is valid until
                    <a href="/windows/desktop/api/webservices/nf-webservices-wsreseterror">WsResetError</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeerror">WsFreeError</a> are called for the error object.
                

The default value is <b>NULL</b>.

### -field WS_FAULT_ERROR_PROPERTY_ACTION:1

An optional <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a> value representing the action to use for the fault.
                    If the length of the string is zero, then no action is present.
                

To get the string value, pass a WS_XML_STRING* to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetfaulterrorproperty">WsGetFaultErrorProperty</a>.
                    The returned string is valid until <a href="/windows/desktop/api/webservices/nf-webservices-wsreseterror">WsResetError</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeerror">WsFreeError</a> 
                    are called for the error object.
                

To set the string value, pass a WS_XML_STRING* to <a href="/windows/desktop/api/webservices/nf-webservices-wssetfaulterrorproperty">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the string.
                

The default value is a zero-length string.

### -field WS_FAULT_ERROR_PROPERTY_HEADER:2

An optional <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> value representing a header to
                    add to the fault message relating to the fault.
                    If the pointer to the XML_BUFFER is <b>NULL</b>, then no header is present.
                

To get the header value, pass a WS_XML_BUFFER** to <a href="/windows/desktop/api/webservices/nf-webservices-wsgetfaulterrorproperty">WsGetFaultErrorProperty</a>.
                    The returned WS_XML_BUFFER is valid until <a href="/windows/desktop/api/webservices/nf-webservices-wsreseterror">WsResetError</a> or <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeerror">WsFreeError</a> 
                    are called for the error object.
                

To set the header value, pass a WS_XML_BUFFER** to <a href="/windows/desktop/api/webservices/nf-webservices-wssetfaulterrorproperty">WsSetFaultErrorProperty</a>.
                    The error object will make a copy of the buffer.
                

The default value is <b>NULL</b>.
