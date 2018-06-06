---
UID: NS:wsdxmldom._WSDXML_TEXT
title: "_WSDXML_TEXT"
author: windows-sdk-content
description: Describes the text in an XML node.
old-location: ncd\wsdxml_text_struct.htm
old-project: WsdApi
ms.assetid: 44b24ddb-b669-43d0-b8db-0a24f7d020d6
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSDXML_TEXT, WSDXML_TEXT structure, _WSDXML_TEXT, ncd.wsdxml_text_struct, wsdxmldom/WSDXML_TEXT
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
req.typenames: WSDXML_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXmldom.h
api_name:
 - WSDXML_TEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



