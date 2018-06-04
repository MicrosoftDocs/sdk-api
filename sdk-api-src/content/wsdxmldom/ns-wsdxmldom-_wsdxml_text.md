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

# _WSDXML_TEXT structure


## -description


Describes the text in an XML node.


## -struct-fields




### -field Node

The current node in a linked list of <a href="https://msdn.microsoft.com/10c918b2-a7b9-4ebb-a884-64877bebb973">WSDXML_NODE</a> structures.


### -field Text

The text contained in the XML node. The maximum length of this string is WSD_MAX_TEXT_LENGTH (8192). The text must consist of UTF-16 encoded characters. The text cannot contain raw XML, as special characters are rendered using the equivalent entity reference. For example,  <code>&lt;</code> is rendered as <code>&amp;lt;</code>.


## -remarks



<b>WSDXML_TEXT</b> is used to represent the contents of an element. Since no type information exists for elements in DOM, the <b>Text</b> member is the exact representation of the element contents from the XML document.



