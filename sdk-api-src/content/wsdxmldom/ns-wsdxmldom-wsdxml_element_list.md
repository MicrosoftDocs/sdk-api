---
UID: NS:wsdxmldom._WSDXML_ELEMENT_LIST
title: WSDXML_ELEMENT_LIST (wsdxmldom.h)
author: windows-sdk-content
description: Represents a node in a linked list of XML elements.
old-location: ncd\wsdxml_element_list_struct.htm
tech.root: WsdApi
ms.assetid: 498fe365-e9a1-490c-a361-2312ea698977
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSDXML_ELEMENT_LIST, WSDXML_ELEMENT_LIST structure, _WSDXML_ELEMENT_LIST, ncd.wsdxml_element_list_struct, wsdxmldom/WSDXML_ELEMENT_LIST
ms.topic: struct
f1_keywords: 
 - "wsdxmldom/WSDXML_ELEMENT_LIST"
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
 - WSDXML_ELEMENT_LIST
product: Windows
targetos: Windows
req.typenames: WSDXML_ELEMENT_LIST
req.redist: 
ms.custom: 19H1
---

# WSDXML_ELEMENT_LIST structure


## -description


Represents a node in a linked list of XML elements.


## -struct-fields




### -field Next

Reference to the next node in the linked list of <b>WSDXML_ELEMENT_LIST</b> structures.


### -field Element

The <a href="https://docs.microsoft.com/windows/desktop/api/wsdxmldom/ns-wsdxmldom-_wsdxml_element">WSDXML_ELEMENT</a> structure referenced by this node.

