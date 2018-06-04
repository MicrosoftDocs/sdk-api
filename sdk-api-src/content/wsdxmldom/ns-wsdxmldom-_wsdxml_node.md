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

# _WSDXML_NODE structure


## -description


Describes an XML node.


## -struct-fields




### -field Parent

Reference to the parent node in a linked list of <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structures.


### -field Next

Reference to the next node in the linked list of <b>WSDXML_NODE</b> structures.


#### - Type

Indicates whether the node is an element or text.



#### ElementType

Node represents an XML element.



#### TextType

Node represents text.


## -remarks



<b>WSDXML_NODE</b> represents an arbitrary node within the DOM tree. Nodes are weakly typed; the <b>Type</b> member must be inspected to determine the actual type of the node, and the node pointer must then be cast to the structure of the appropriate type (see <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> and <a href="https://msdn.microsoft.com/44b24ddb-b669-43d0-b8db-0a24f7d020d6">WSDXML_TEXT</a>) to obtain the node contents. <b>Parent</b> points to the containing element for the current node, and <b>Next</b> points to any nodes at the same level as the current node.



