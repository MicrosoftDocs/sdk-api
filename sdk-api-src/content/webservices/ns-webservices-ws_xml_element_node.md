---
UID: NS:webservices._WS_XML_ELEMENT_NODE
title: WS_XML_ELEMENT_NODE (webservices.h)
description: Represents a start element in xml (e.g.
helpviewer_keywords: ["WS_XML_ELEMENT_NODE","WS_XML_ELEMENT_NODE structure [Web Services for Windows]","webservices/WS_XML_ELEMENT_NODE","wsw.ws_xml_element_node"]
old-location: wsw\ws_xml_element_node.htm
tech.root: wsw
ms.assetid: 32157ddf-ace2-49dc-85d7-b04e25e85693
ms.date: 12/05/2018
ms.keywords: WS_XML_ELEMENT_NODE, WS_XML_ELEMENT_NODE structure [Web Services for Windows], webservices/WS_XML_ELEMENT_NODE, wsw.ws_xml_element_node
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
req.typenames: WS_XML_ELEMENT_NODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WS_XML_ELEMENT_NODE
 - webservices/_WS_XML_ELEMENT_NODE
 - WS_XML_ELEMENT_NODE
 - webservices/WS_XML_ELEMENT_NODE
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
 - WS_XML_ELEMENT_NODE
---

# WS_XML_ELEMENT_NODE structure


## -description

Represents a start element in xml (e.g. 
        &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)

## -struct-fields

### -field node

The base type for all types that derive from <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">WS_XML_NODE</a>.

### -field prefix

The prefix of the element.  In the example, it refers to "a".  Empty prefixes are represented by a zero length <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_string">WS_XML_STRING</a>.

### -field localName

The localName of the element.  In the example, it refers to "purchaseOrder".

### -field ns

The resolved namespace of the prefix.  In the example, it refers to "http://tempuri.org".

### -field attributeCount

The number of attributes on the element.  In the example, it would be 2.

### -field attributes

The array of attributes for the element.

### -field isEmpty

Whether the element is an empty element or not.  In the example, it would be <b>FALSE</b>.