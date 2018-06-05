---
UID: NS:wsdxmldom._WSDXML_ELEMENT_LIST
title: "_WSDXML_ELEMENT_LIST"
author: windows-sdk-content
description: Represents a node in a linked list of XML elements.
old-location: ncd\wsdxml_element_list_struct.htm
old-project: WsdApi
ms.assetid: 498fe365-e9a1-490c-a361-2312ea698977
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSDXML_ELEMENT_LIST, WSDXML_ELEMENT_LIST structure, _WSDXML_ELEMENT_LIST, ncd.wsdxml_element_list_struct, wsdxmldom/WSDXML_ELEMENT_LIST
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSDXML_ELEMENT_LIST
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdXmldom.h
api_name:
-	WSDXML_ELEMENT_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSDXML_ELEMENT_LIST structure


## -description


Represents a node in a linked list of XML elements.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSDXML_ELEMENT_LIST</b> structures.


### -field Element

The <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure referenced by this node.

