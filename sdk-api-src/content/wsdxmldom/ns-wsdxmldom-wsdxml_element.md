---
UID: NS:wsdxmldom._WSDXML_ELEMENT
title: WSDXML_ELEMENT (wsdxmldom.h)
description: Describes an XML element.
helpviewer_keywords: ["WSDXML_ELEMENT","WSDXML_ELEMENT structure","_WSDXML_ELEMENT","ncd.wsdxml_element_struct","wsdxmldom/WSDXML_ELEMENT"]
old-location: ncd\wsdxml_element_struct.htm
tech.root: ncd
ms.assetid: 727149b4-31b0-4fd8-b0fa-eb773edb171e
ms.date: 12/05/2018
ms.keywords: WSDXML_ELEMENT, WSDXML_ELEMENT structure, _WSDXML_ELEMENT, ncd.wsdxml_element_struct, wsdxmldom/WSDXML_ELEMENT
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
req.typenames: WSDXML_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDXML_ELEMENT
 - wsdxmldom/_WSDXML_ELEMENT
 - WSDXML_ELEMENT
 - wsdxmldom/WSDXML_ELEMENT
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
 - WSDXML_ELEMENT
---

# WSDXML_ELEMENT structure


## -description

Describes an XML element.

## -struct-fields

### -field Node

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_node">WSDXML_NODE</a> structure that specifies the parent element, next sibling and type of the node.

### -field Name

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that specifies name.

### -field FirstAttribute

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_attribute">WSDXML_ATTRIBUTE</a> structure that specifies the first attribute.

### -field FirstChild

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_node">WSDXML_NODE</a> structure that specifies the first child.

### -field PrefixMappings

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_prefix_mapping">WSDXML_PREFIX_MAPPING</a> structure that specifies the prefix mappings.

## -remarks

<b>WSDXML_ELEMENT</b> represents an XML element in the DOM tree. The <b>Name</b> member can be used to determine the name and namespace of this element. <b>FirstAttribute</b> points to any attributes, and <b>FirstChild</b> points to anything contained within the element.