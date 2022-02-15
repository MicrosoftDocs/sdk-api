---
UID: NE:webservices.__unnamed_enum_6
title: WS_XML_NODE_TYPE (webservices.h)
description: The type of WS_XML_NODE structure.
helpviewer_keywords: ["WS_XML_NODE_TYPE","WS_XML_NODE_TYPE enumeration [Web Services for Windows]","WS_XML_NODE_TYPE_BOF","WS_XML_NODE_TYPE_CDATA","WS_XML_NODE_TYPE_COMMENT","WS_XML_NODE_TYPE_ELEMENT","WS_XML_NODE_TYPE_END_CDATA","WS_XML_NODE_TYPE_END_ELEMENT","WS_XML_NODE_TYPE_EOF","WS_XML_NODE_TYPE_TEXT","webservices/WS_XML_NODE_TYPE","webservices/WS_XML_NODE_TYPE_BOF","webservices/WS_XML_NODE_TYPE_CDATA","webservices/WS_XML_NODE_TYPE_COMMENT","webservices/WS_XML_NODE_TYPE_ELEMENT","webservices/WS_XML_NODE_TYPE_END_CDATA","webservices/WS_XML_NODE_TYPE_END_ELEMENT","webservices/WS_XML_NODE_TYPE_EOF","webservices/WS_XML_NODE_TYPE_TEXT","wsw.ws_xml_node_type"]
old-location: wsw\ws_xml_node_type.htm
tech.root: wsw
ms.assetid: eddef5db-432d-4615-9f0f-a712dffe42ab
ms.date: 12/05/2018
ms.keywords: WS_XML_NODE_TYPE, WS_XML_NODE_TYPE enumeration [Web Services for Windows], WS_XML_NODE_TYPE_BOF, WS_XML_NODE_TYPE_CDATA, WS_XML_NODE_TYPE_COMMENT, WS_XML_NODE_TYPE_ELEMENT, WS_XML_NODE_TYPE_END_CDATA, WS_XML_NODE_TYPE_END_ELEMENT, WS_XML_NODE_TYPE_EOF, WS_XML_NODE_TYPE_TEXT, webservices/WS_XML_NODE_TYPE, webservices/WS_XML_NODE_TYPE_BOF, webservices/WS_XML_NODE_TYPE_CDATA, webservices/WS_XML_NODE_TYPE_COMMENT, webservices/WS_XML_NODE_TYPE_ELEMENT, webservices/WS_XML_NODE_TYPE_END_CDATA, webservices/WS_XML_NODE_TYPE_END_ELEMENT, webservices/WS_XML_NODE_TYPE_EOF, webservices/WS_XML_NODE_TYPE_TEXT, wsw.ws_xml_node_type
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
req.typenames: WS_XML_NODE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_XML_NODE_TYPE
 - webservices/WS_XML_NODE_TYPE
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
 - WS_XML_NODE_TYPE
---

# WS_XML_NODE_TYPE enumeration


## -description

The type of <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">WS_XML_NODE</a> structure.

## -enum-fields

### -field WS_XML_NODE_TYPE_ELEMENT:1

A start element. (e.g. &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)

### -field WS_XML_NODE_TYPE_TEXT:2

Element, attribute, or CDATA content.

### -field WS_XML_NODE_TYPE_END_ELEMENT:3

An end element. (e.g. &lt;/purchaseOrder&gt;)

### -field WS_XML_NODE_TYPE_COMMENT:4

A comment. (For example, &lt;!--The message follows--&gt;)

### -field WS_XML_NODE_TYPE_CDATA:6

The start of a CDATA section (i.e. &lt;![CDATA[)

### -field WS_XML_NODE_TYPE_END_CDATA:7

The end of a CDATA section (i.e. ]]&gt;)

### -field WS_XML_NODE_TYPE_EOF:8

The final node of an xml stream.

### -field WS_XML_NODE_TYPE_BOF:9

The first node of an xml stream.

## -remarks

The BNF for node types within a document is:
      


``` syntax

Xml := StartInput Whitespace Element Whitespace EndInput
Whitespace := (Text | Comment)* // Text is whitespace only
Element := StartElement ElementContent EndElement
ElementContent := (Element | Text | Comment | CData)*
StartElement := WS_XML_NODE_TYPE_ELEMENT
EndElement := WS_XML_NODE_TYPE_END_ELEMENT
Text := WS_XML_NODE_TYPE_TEXT
Comment := WS_XML_NODE_TYPE_COMMENT
CData := WS_XML_NODE_TYPE_CDATA Text* WS_XML_NODE_TYPE_END_CDATA
StartInput := WS_XML_NODE_TYPE_BOF
EndInput := WS_XML_NODE_TYPE_EOF
```

