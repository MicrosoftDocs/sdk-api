---
UID: NS:xpsobjectmodel.__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021
title: XPS_GLYPH_INDEX (xpsobjectmodel.h)
description: Describes the placement and location of a glyph.
helpviewer_keywords: ["XPS_GLYPH_INDEX","XPS_GLYPH_INDEX structure [XPS Documents and Packaging]","xps.xps_glyph_index","xpsobjectmodel/XPS_GLYPH_INDEX"]
old-location: xps\xps_glyph_index.htm
tech.root: printdocs
ms.assetid: 0ea30e0f-f32b-4a38-9591-27cb1fe7f234
ms.date: 12/05/2018
ms.keywords: XPS_GLYPH_INDEX, XPS_GLYPH_INDEX structure [XPS Documents and Packaging], xps.xps_glyph_index, xpsobjectmodel/XPS_GLYPH_INDEX
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
req.typenames: XPS_GLYPH_INDEX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021
 - xpsobjectmodel/__MIDL___MIDL_itf_xpsobjectmodel_0000_0000_0021
 - XPS_GLYPH_INDEX
 - xpsobjectmodel/XPS_GLYPH_INDEX
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
 - XPS_GLYPH_INDEX
---

# XPS_GLYPH_INDEX structure


## -description

Describes the placement and location of a glyph.

## -struct-fields

### -field index

The index of a glyph in the physical font.

### -field advanceWidth

Indicates the  placement of the glyph that follows,  relative to the origin of the current glyph. Measured in hundredths of the font's em-size.

### -field horizontalOffset

The horizontal distance, in the effective coordinate space, by which to move the glyph from the glyph's origin. Measured in hundredths of the font's em-size.

### -field verticalOffset

The vertical distance, in the effective coordinate space, by which to move the glyph from the glyph's origin. Measured in hundredths of the font's  em-size.

## -see-also

<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>

