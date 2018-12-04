---
UID: NS:wsdxmldom._WSDXML_NODE
title: "_WSDXML_NODE"
author: windows-sdk-content
description: Describes an XML node.
old-location: ncd\wsdxml_node_struct.htm
tech.root: wsdapi
ms.assetid: 10c918b2-a7b9-4ebb-a884-64877bebb973
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WSDXML_NODE, WSDXML_NODE structure, _WSDXML_NODE, ncd.wsdxml_node_struct, wsdxmldom/WSDXML_NODE
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
 - WsdXmldom.h
api_name:
 - WSDXML_NODE
product: Windows
targetos: Windows
req.typenames: WSDXML_NODE
req.redist: 
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



