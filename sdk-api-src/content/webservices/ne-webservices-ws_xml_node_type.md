---
UID: NE:webservices.__unnamed_enum_6
title: WS_XML_NODE_TYPE
author: windows-sdk-content
description: The type of WS_XML_NODE structure.
old-location: wsw\ws_xml_node_type.htm
tech.root: wsw
ms.assetid: eddef5db-432d-4615-9f0f-a712dffe42ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_XML_NODE_TYPE, WS_XML_NODE_TYPE enumeration [Web Services for Windows], WS_XML_NODE_TYPE_BOF, WS_XML_NODE_TYPE_CDATA, WS_XML_NODE_TYPE_COMMENT, WS_XML_NODE_TYPE_ELEMENT, WS_XML_NODE_TYPE_END_CDATA, WS_XML_NODE_TYPE_END_ELEMENT, WS_XML_NODE_TYPE_EOF, WS_XML_NODE_TYPE_TEXT, webservices/WS_XML_NODE_TYPE, webservices/WS_XML_NODE_TYPE_BOF, webservices/WS_XML_NODE_TYPE_CDATA, webservices/WS_XML_NODE_TYPE_COMMENT, webservices/WS_XML_NODE_TYPE_ELEMENT, webservices/WS_XML_NODE_TYPE_END_CDATA, webservices/WS_XML_NODE_TYPE_END_ELEMENT, webservices/WS_XML_NODE_TYPE_EOF, webservices/WS_XML_NODE_TYPE_TEXT, wsw.ws_xml_node_type
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_XML_NODE_TYPE
product: Windows
targetos: Windows
req.typenames: WS_XML_NODE_TYPE
req.redist: 
---

# WS_XML_NODE_TYPE enumeration


## -description


The type of <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">WS_XML_NODE</a> structure.
      


## -enum-fields




### -field WS_XML_NODE_TYPE_ELEMENT

A start element. (e.g. &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)
        


### -field WS_XML_NODE_TYPE_TEXT

Element, attribute, or CDATA content.
        


### -field WS_XML_NODE_TYPE_END_ELEMENT

An end element. (e.g. &lt;/purchaseOrder&gt;)
        


### -field WS_XML_NODE_TYPE_COMMENT

A comment. (For example, &lt;!--The message follows--&gt;)
        


### -field WS_XML_NODE_TYPE_CDATA

The start of a CDATA section (i.e. &lt;![CDATA[)
        


### -field WS_XML_NODE_TYPE_END_CDATA

The end of a CDATA section (i.e. ]]&gt;)
        


### -field WS_XML_NODE_TYPE_EOF

The final node of an xml stream.
        


### -field WS_XML_NODE_TYPE_BOF

The first node of an xml stream.
        


## -remarks



The BNF for node types within a document is:
      

<pre class="syntax" xml:space="preserve"><code>
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
EndInput := WS_XML_NODE_TYPE_EOF</code></pre>


