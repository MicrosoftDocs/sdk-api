---
UID: NE:dwrite_3.DWRITE_FONT_FAMILY_MODEL
title: DWRITE_FONT_FAMILY_MODEL
description: Defines constants that specify how font families are grouped together.
helpviewer_keywords: ["DWRITE_FONT_FAMILY_MODEL","DWRITE_FONT_FAMILY_MODEL enumeration [Direct Write]","directwrite.dwrite_font_family_model","dwrite_3/DWRITE_FONT_FAMILY_MODEL"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: DWRITE_FONT_FAMILY_MODEL, DWRITE_FONT_FAMILY_MODEL enumeration [Direct Write], directwrite.dwrite_font_family_model, dwrite_3/DWRITE_FONT_FAMILY_MODEL
req.construct-type: enumeration
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
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
req.typenames: 
req.redist: 
f1_keywords:
 - DWRITE_FONT_FAMILY_MODEL
 - dwrite_3/DWRITE_FONT_FAMILY_MODEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite_3.h
api_name:
 - DWRITE_FONT_FAMILY_MODEL
---

## -description

Defines constants that specify how font families are grouped together. Used by [IDWriteFontCollection2](./nn-dwrite_3-idwritefontcollection2.md), for example.

## -enum-fields

### -field DWRITE_FONT_FAMILY_MODEL_TYPOGRAPHIC

Families are grouped by the typographic family name preferred by the font author. The family can contain as many faces as the font author wants. This corresponds to <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id">DWRITE_FONT_PROPERTY_ID_TYPOGRAPHIC_FAMILY_NAME</a>.

### -field DWRITE_FONT_FAMILY_MODEL_WEIGHT_STRETCH_STYLE

Families are grouped by the weight-stretch-style family name, where all faces that differ only by those three axes are grouped into the same family, but any other axes go into a distinct family. For example, the Sitka family with six different optical sizes yields six separate families (Sitka Caption, Display, Text, Subheading, Heading, Banner...). This corresponds to <a href="/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id">DWRITE_FONT_PROPERTY_ID_WEIGHT_STRETCH_STYLE_FAMILY_NAME</a>.

## -remarks

## -see-also
