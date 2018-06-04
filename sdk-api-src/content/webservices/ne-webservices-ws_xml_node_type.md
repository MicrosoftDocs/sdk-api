---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


