---
UID: NS:webservices._WS_XML_ELEMENT_NODE
title: "_WS_XML_ELEMENT_NODE"
author: windows-driver-content
description: Represents a start element in xml (e.g.
old-location: wsw\ws_xml_element_node.htm
old-project: wsw
ms.assetid: 32157ddf-ace2-49dc-85d7-b04e25e85693
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_XML_ELEMENT_NODE, WS_XML_ELEMENT_NODE structure [Web Services for Windows], _WS_XML_ELEMENT_NODE, webservices/WS_XML_ELEMENT_NODE, wsw.ws_xml_element_node
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: WS_XML_ELEMENT_NODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_ELEMENT_NODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_ELEMENT_NODE structure


## -description



        Represents a start element in xml (e.g. 
        &lt;a:purchaseOrder xmlns:a="http://tempuri.org" id="5"&gt;)
      


## -struct-fields




### -field node


          The base type for all types that derive from <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">WS_XML_NODE</a>.
        


### -field prefix


          The prefix of the element.  In the example, it refers to "a".  Empty prefixes are represented by a zero length <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a>.
        


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
        

