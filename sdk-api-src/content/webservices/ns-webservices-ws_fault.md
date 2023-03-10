---
UID: NS:webservices._WS_FAULT
title: WS_FAULT (webservices.h)
description: A Fault is a value carried in the body of a message which conveys a processing failure. Faults are modeled using the WS_FAULT structure.
helpviewer_keywords: ["WS_FAULT","WS_FAULT structure [Web Services for Windows]","webservices/WS_FAULT","wsw.ws_fault"]
old-location: wsw\ws_fault.htm
tech.root: wsw
ms.assetid: 7fe0b142-04a1-4a92-99ca-523412f7c94e
ms.date: 12/05/2018
ms.keywords: WS_FAULT, WS_FAULT structure [Web Services for Windows], webservices/WS_FAULT, wsw.ws_fault
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
req.typenames: WS_FAULT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_FAULT
 - webservices/_WS_FAULT
 - WS_FAULT
 - webservices/WS_FAULT
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
 - WS_FAULT
---

# WS_FAULT structure


## -description

A Fault is a value carried in the body of a message which conveys a 
                processing failure.  Faults are modeled using the <b>WS_FAULT</b> structure.

## -struct-fields

### -field code

The head of the list of fault codes which identifies the type of fault.
                

The fault codes are ordered from most generic to most specific.
                    There must be at least one fault code.  The first fault code
                    must correspond to a fault code defined by SOAP.
                    For <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, only the most specific fault code
                    is serialized (the first one in the list).
                

If the namespace URI of the first fault code is the empty string,
                    then the first fault code will be transformed as follows
                    when the fault is serialized, as follows:
                

<ul>
<li>The appropriate SOAP namespace will be used based on the 
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION</a>.
                    </li>
<li>If the local name is "Sender" when using 
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, then "Client" will be used instead.
                    </li>
<li>If the local name is "Receiver" when using
                    <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, then "Server" will be used instead.
                </li>
</ul>
These transformations allow a SOAP fault code
                    to be specified without having to worry about which SOAP version is used.

### -field reasons

The text describing the fault.  This is an array to allow for different
                    languages.

### -field reasonCount

The number of reasons in the reasons array.  This would be more than one
                    if the text was represented in multiple languages.  There must be at
                    least one fault reason.
                

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, only the first reason is serialized.

### -field actor

The name of the processor that caused the fault.  If the string is zero
                    length, then it's assumed to be the endpoint.

### -field node

The location of the processor that caused the fault.  If the string is zero
                    length, then it's assumed to be the endpoint.
                

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, this value is not serialized.

### -field detail

The fault detail allows for XML content to be included along with the fault.  If
                    there is no detail, then this field may be <b>NULL</b>.
                

For <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION_SOAP_1_1</a>, this should only be used if the fault
                    does not relate to processing of a header of the message.  Faults relating to
                    headers should use a custom header to relay information about the fault.
                

If there is detail for the fault, the <a href="/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> should contain 
                    an element that corresponds to the detail element of a SOAP fault.  The
                    fault-specific XML content is contained within the detail element.
                    The local name and namespace of the element are ignored; they are replaced with
                    the appropriate element name according to the <a href="/windows/desktop/api/webservices/ne-webservices-ws_envelope_version">WS_ENVELOPE_VERSION</a> when the detail element is written.