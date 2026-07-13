---
UID: NE:d2d1svg.D2D1_SVG_ATTRIBUTE_STRING_TYPE
title: D2D1_SVG_ATTRIBUTE_STRING_TYPE (d2d1svg.h)
description: Defines the type of SVG string attribute to set or get.
helpviewer_keywords: ["D2D1_SVG_ATTRIBUTE_STRING_TYPE","D2D1_SVG_ATTRIBUTE_STRING_TYPE enumeration [Direct2D]","D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD","D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID","D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG","d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE","d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD","d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID","d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG","direct2d.d2d1_svg_attribute_string_type"]
old-location: direct2d\d2d1_svg_attribute_string_type.htm
tech.root: Direct2D
ms.assetid: 71991A28-FEA0-42A1-B5D0-DA13BBA77500
ms.date: 12/05/2018
ms.keywords: D2D1_SVG_ATTRIBUTE_STRING_TYPE, D2D1_SVG_ATTRIBUTE_STRING_TYPE enumeration [Direct2D], D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD, D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID, D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG, d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE, d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD, d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID, d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG, direct2d.d2d1_svg_attribute_string_type
req.header: d2d1svg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: D2D1_SVG_ATTRIBUTE_STRING_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_SVG_ATTRIBUTE_STRING_TYPE
 - d2d1svg/D2D1_SVG_ATTRIBUTE_STRING_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1svg.h
api_name:
 - D2D1_SVG_ATTRIBUTE_STRING_TYPE
---

# D2D1_SVG_ATTRIBUTE_STRING_TYPE enumeration


## -description

Defines the type of SVG string attribute to set or get.

## -enum-fields

### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_SVG:0

The attribute is a string in the same form as it would appear in the SVG XML.
          Note that when getting values of this type, the value returned may not exactly match the value that was set. Instead, the output value is a normalized version
          of the value. For example, an input color of 'red' may be output as '#FF0000'.

### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_ID:1

The attribute is an element ID.

### -field D2D1_SVG_ATTRIBUTE_STRING_TYPE_FORCE_DWORD:0xffffffff

