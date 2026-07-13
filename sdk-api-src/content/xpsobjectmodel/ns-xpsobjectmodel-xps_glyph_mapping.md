---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022
title: XPS_GLYPH_MAPPING (xpsobjectmodel.h)
description: Describes a glyph-to-index mapping.
helpviewer_keywords: ["XPS_GLYPH_MAPPING","XPS_GLYPH_MAPPING structure [XPS Documents and Packaging]","xps.xps_glyph_mapping","xpsobjectmodel/XPS_GLYPH_MAPPING"]
old-location: xps\xps_glyph_mapping.htm
tech.root: xps
ms.assetid: 5cc76cba-66e4-4853-969b-a99ec7bb22f3
ms.date: 12/05/2018
ms.keywords: XPS_GLYPH_MAPPING, XPS_GLYPH_MAPPING structure [XPS Documents and Packaging], xps.xps_glyph_mapping, xpsobjectmodel/XPS_GLYPH_MAPPING
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XPS_GLYPH_MAPPING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0022
 - XPS_GLYPH_MAPPING
 - xpsobjectmodel/XPS_GLYPH_MAPPING
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xpsobjectmodel.h
api_name:
 - XPS_GLYPH_MAPPING
---

# XPS_GLYPH_MAPPING structure


## -description

Describes a glyph-to-index mapping.

## -struct-fields

### -field unicodeStringStart

Index of the first Unicode character in the mapping string.

### -field unicodeStringLength

Number of characters in the mapping string.

### -field glyphIndicesStart

The glyph array's first  index that corresponds to <b>unicodeStringStart</b>.

### -field glyphIndicesLength

Length of index mapping.

## -see-also

<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>

