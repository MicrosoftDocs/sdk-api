---
UID: NS:wsdxmldom._WSDXML_ELEMENT
title: "_WSDXML_ELEMENT"
author: windows-driver-content
description: Describes an XML element.
old-location: ncd\wsdxml_element_struct.htm
old-project: WsdApi
ms.assetid: 727149b4-31b0-4fd8-b0fa-eb773edb171e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSDXML_ELEMENT, WSDXML_ELEMENT structure, _WSDXML_ELEMENT, ncd.wsdxml_element_struct, wsdxmldom/WSDXML_ELEMENT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdxmldom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdXml.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSDXML_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdXmldom.h
api_name:
-	WSDXML_ELEMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSDXML_ELEMENT structure


## -description


Describes an XML element.


## -struct-fields




### -field Node

Reference to a <a href="https://msdn.microsoft.com/10c918b2-a7b9-4ebb-a884-64877bebb973">WSDXML_NODE</a> structure that specifies the parent element, next sibling and type of the node. 



### -field Name

Reference to a <a href="https://msdn.microsoft.com/9dce71d2-700c-4f86-9308-dee6a69010bb">WSDXML_NAME</a> structure that specifies name. 



### -field FirstAttribute

Reference to a <a href="https://msdn.microsoft.com/2697d30d-17c7-417d-a02b-c4427987ec4b">WSDXML_ATTRIBUTE</a> structure that specifies the first attribute. 



### -field FirstChild

Reference to a <a href="https://msdn.microsoft.com/10c918b2-a7b9-4ebb-a884-64877bebb973">WSDXML_NODE</a> structure that specifies the first child. 



### -field PrefixMappings

Reference to a <a href="https://msdn.microsoft.com/d49a155a-a71b-4038-86a8-eb398db64e72">WSDXML_PREFIX_MAPPING</a> structure that specifies the prefix mappings. 



## -remarks



<b>WSDXML_ELEMENT</b> represents an XML element in the DOM tree. The <b>Name</b> member can be used to determine the name and namespace of this element. <b>FirstAttribute</b> points to any attributes, and <b>FirstChild</b> points to anything contained within the element. 



