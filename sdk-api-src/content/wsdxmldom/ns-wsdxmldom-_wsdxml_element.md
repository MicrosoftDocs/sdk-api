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



