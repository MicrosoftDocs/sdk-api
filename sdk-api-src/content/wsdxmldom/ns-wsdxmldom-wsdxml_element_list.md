---
UID: NS:wsdxmldom._WSDXML_ELEMENT_LIST
title: WSDXML_ELEMENT_LIST (wsdxmldom.h)
description: Represents a node in a linked list of XML elements.
helpviewer_keywords: ["WSDXML_ELEMENT_LIST","WSDXML_ELEMENT_LIST structure","_WSDXML_ELEMENT_LIST","ncd.wsdxml_element_list_struct","wsdxmldom/WSDXML_ELEMENT_LIST"]
old-location: ncd\wsdxml_element_list_struct.htm
tech.root: ncd
ms.assetid: 498fe365-e9a1-490c-a361-2312ea698977
ms.date: 12/05/2018
ms.keywords: WSDXML_ELEMENT_LIST, WSDXML_ELEMENT_LIST structure, _WSDXML_ELEMENT_LIST, ncd.wsdxml_element_list_struct, wsdxmldom/WSDXML_ELEMENT_LIST
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
targetos: Windows
req.typenames: WSDXML_ELEMENT_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDXML_ELEMENT_LIST
 - wsdxmldom/_WSDXML_ELEMENT_LIST
 - WSDXML_ELEMENT_LIST
 - wsdxmldom/WSDXML_ELEMENT_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdXmldom.h
api_name:
 - WSDXML_ELEMENT_LIST
---

# WSDXML_ELEMENT_LIST structure


## -description

Represents a node in a linked list of XML elements.

## -struct-fields

### -field Next

Reference to the next node in the linked list of <b>WSDXML_ELEMENT_LIST</b> structures.

### -field Element

The <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure referenced by this node.