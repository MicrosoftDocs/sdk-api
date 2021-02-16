---
UID: NS:wsdxmldom._WSDXML_PREFIX_MAPPING
title: WSDXML_PREFIX_MAPPING (wsdxmldom.h)
description: Describes an XML namespace prefix.
helpviewer_keywords: ["WSDXML_PREFIX_MAPPING","WSDXML_PREFIX_MAPPING structure","_WSDXML_PREFIX_MAPPING","ncd.wsdxml_prefix_mapping_struct","wsdxmldom/WSDXML_PREFIX_MAPPING"]
old-location: ncd\wsdxml_prefix_mapping_struct.htm
tech.root: ncd
ms.assetid: d49a155a-a71b-4038-86a8-eb398db64e72
ms.date: 12/05/2018
ms.keywords: WSDXML_PREFIX_MAPPING, WSDXML_PREFIX_MAPPING structure, _WSDXML_PREFIX_MAPPING, ncd.wsdxml_prefix_mapping_struct, wsdxmldom/WSDXML_PREFIX_MAPPING
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
req.typenames: WSDXML_PREFIX_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSDXML_PREFIX_MAPPING
 - wsdxmldom/_WSDXML_PREFIX_MAPPING
 - WSDXML_PREFIX_MAPPING
 - wsdxmldom/WSDXML_PREFIX_MAPPING
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
 - WSDXML_PREFIX_MAPPING
---

# WSDXML_PREFIX_MAPPING structure


## -description

Describes an XML namespace prefix.

## -struct-fields

### -field Refs

The number of references to the mapping. When the value reaches zero, the mapping is deleted.

### -field Next

Reference to the next node in a linked list of <b>WSDXML_PREFIX_MAPPING</b> structures.

### -field Space

Reference to a <a href="/windows/desktop/api/wsdxmldom/ns-wsdxmldom-wsdxml_namespace">WSDXML_NAMESPACE</a> structure.

### -field Prefix

The text of the XML prefix.