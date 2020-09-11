---
UID: NE:webservices.__unnamed_enum_85
title: WS_TYPE_MAPPING (webservices.h)
description: How a WS_TYPE maps to or from XML when serialized or deserialized.
helpviewer_keywords: ["WS_ANY_ELEMENT_TYPE_MAPPING","WS_ATTRIBUTE_TYPE_MAPPING","WS_ELEMENT_CONTENT_TYPE_MAPPING","WS_ELEMENT_TYPE_MAPPING","WS_TYPE_MAPPING","WS_TYPE_MAPPING enumeration [Web Services for Windows]","webservices/WS_ANY_ELEMENT_TYPE_MAPPING","webservices/WS_ATTRIBUTE_TYPE_MAPPING","webservices/WS_ELEMENT_CONTENT_TYPE_MAPPING","webservices/WS_ELEMENT_TYPE_MAPPING","webservices/WS_TYPE_MAPPING","wsw.ws_type_mapping"]
old-location: wsw\ws_type_mapping.htm
tech.root: wsw
ms.assetid: 31e4abad-d007-41ae-bf51-fa693e8b8ae5
ms.date: 12/05/2018
ms.keywords: WS_ANY_ELEMENT_TYPE_MAPPING, WS_ATTRIBUTE_TYPE_MAPPING, WS_ELEMENT_CONTENT_TYPE_MAPPING, WS_ELEMENT_TYPE_MAPPING, WS_TYPE_MAPPING, WS_TYPE_MAPPING enumeration [Web Services for Windows], webservices/WS_ANY_ELEMENT_TYPE_MAPPING, webservices/WS_ATTRIBUTE_TYPE_MAPPING, webservices/WS_ELEMENT_CONTENT_TYPE_MAPPING, webservices/WS_ELEMENT_TYPE_MAPPING, webservices/WS_TYPE_MAPPING, wsw.ws_type_mapping
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
req.typenames: WS_TYPE_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_TYPE_MAPPING
 - webservices/WS_TYPE_MAPPING
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
 - WS_TYPE_MAPPING
---

# WS_TYPE_MAPPING enumeration


## -description

How a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> maps to or from XML when serialized
                or deserialized.

## -enum-fields

### -field WS_ELEMENT_TYPE_MAPPING

This is used when reading or writing an element where the type
                    corresponds to the type of the element.
                    The definition of the type may include mappings to attributes,
                    text, or child elements of the element.
                

The following calling sequence is used when writing an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartElement(...)
WsWriteType(..., WS_ELEMENT_TYPE_MAPPING, ...)
WsWriteEndElement(...)</code></pre>
The following calling sequence is used when reading an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)?
WsReadType(..., WS_ELEMENT_TYPE_MAPPING, ...)</code></pre>

### -field WS_ATTRIBUTE_TYPE_MAPPING

This is used when reading or writing the value of a single attribute.  The definition
                    of the type must not require any mappings to attributes or child elements.
                

The following calling sequence is used when writing an attribute value.
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartAttribute(...)
WsWriteType(..., WS_ATTRIBUTE_TYPE_MAPPING, ...)
WsWriteEndAttribute(...)</code></pre>
The following calling sequence is used when reading an attribute value.
                

<pre class="syntax" xml:space="preserve"><code>
WsFindAttribute(...)
WsReadStartAttribute(...)
WsReadType(..., WS_ATTRIBUTE_TYPE_MAPPING, ...)
WsReadEndAttribute(...)</code></pre>

### -field WS_ELEMENT_CONTENT_TYPE_MAPPING

This is used when when the type corresponds to all or part of the 
                    content (text and child elements) of an element.
                    The definition of the type may include mappings to text or child
                    elements, but must not include any attributes.
                

The following calling sequence is used when writing the contents
                    of an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteStartElement(...)
// Write attributes, if any
// Write other element content, if any
WsWriteType(..., WS_ELEMENT_CONTENT_TYPE_MAPPING, ...)
// Write other element content, if any
WsWriteEndElement(...)</code></pre>
The following calling sequence is used when reading the contents of
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)
// Read attributes, if any
WsReadStartElement(...)
// Read other element content, if any
WsReadType(..., WS_ELEMENT_CONTENT_TYPE_MAPPING, ...)
// Read other element content, if any
WsReadEndElement(...)</code></pre>

### -field WS_ANY_ELEMENT_TYPE_MAPPING

This is used when when the type corresponds to the complete
                    element, including the name and namespace of the element.
                    The definition may include attributes and child elements
                    and text.
                

The following calling sequence is used when writing 
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsWriteType(..., WS_ANY_ELEMENT_TYPE_MAPPING, ...)</code></pre>
The following calling sequence is used when reading the contents of
                    an element:
                

<pre class="syntax" xml:space="preserve"><code>
WsReadToStartElement(...)?
WsReadType(..., WS_ANY_ELEMENT_TYPE_MAPPING, ...)</code></pre>

## -remarks

See the documentation for each <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ne-webservices-ws_type">WS_TYPE</a> 
                for which <b>WS_TYPE_MAPPING</b> values are supported.

