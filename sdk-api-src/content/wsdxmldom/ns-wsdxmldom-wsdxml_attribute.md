---
UID: NS:wsdxmldom._WSDXML_ATTRIBUTE
title: WSDXML_ATTRIBUTE (wsdxmldom.h)
description: Describes an XML attribute.
helpviewer_keywords: ["WSDXML_ATTRIBUTE","WSDXML_ATTRIBUTE structure","_WSDXML_ATTRIBUTE","ncd.wsdxml_attribute_struct","wsdxmldom/WSDXML_ATTRIBUTE"]
old-location: ncd\wsdxml_attribute_struct.htm
tech.root: ncd
ms.assetid: 2697d30d-17c7-417d-a02b-c4427987ec4b
ms.date: 12/05/2018
ms.keywords: WSDXML_ATTRIBUTE, WSDXML_ATTRIBUTE structure, _WSDXML_ATTRIBUTE, ncd.wsdxml_attribute_struct, wsdxmldom/WSDXML_ATTRIBUTE
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
req.typenames: WSDXML_ATTRIBUTE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDXML_ATTRIBUTE
 - wsdxmldom/_WSDXML_ATTRIBUTE
 - WSDXML_ATTRIBUTE
 - wsdxmldom/WSDXML_ATTRIBUTE
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
 - WSDXML_ATTRIBUTE
---

# WSDXML_ATTRIBUTE structure


## -description

Describes an XML attribute.

## -struct-fields

### -field Element

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_element">WSDXML_ELEMENT</a> structure that specifies parent element of the attribute.

### -field Next

Reference to a <b>WSDXML_ATTRIBUTE</b> structure that specifies the next sibling attribute, if any.

### -field Name

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_name">WSDXML_NAME</a> structure that specifies the qualified name of the attribute.

### -field Value

The value of the attribute.

## -remarks

<b>WSDXML_ATTRIBUTE</b> is used to describe attribute values in an XML element.