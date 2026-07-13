---
UID: NE:dwrite_3.DWRITE_FONT_PROPERTY_ID
title: DWRITE_FONT_PROPERTY_ID (dwrite_3.h)
description: Identifies a string in a font.
helpviewer_keywords: ["DWRITE_FONT_PROPERTY_ID","DWRITE_FONT_PROPERTY_ID enumeration [Direct Write]","DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG","DWRITE_FONT_PROPERTY_ID_FACE_NAME","DWRITE_FONT_PROPERTY_ID_FAMILY_NAME","DWRITE_FONT_PROPERTY_ID_FULL_NAME","DWRITE_FONT_PROPERTY_ID_NONE","DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME","DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME","DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG","DWRITE_FONT_PROPERTY_ID_STRETCH","DWRITE_FONT_PROPERTY_ID_STYLE","DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG","DWRITE_FONT_PROPERTY_ID_TOTAL","DWRITE_FONT_PROPERTY_ID_WEIGHT","DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME","directwrite.dwrite_font_property_id","dwrite_3/DWRITE_FONT_PROPERTY_ID","dwrite_3/DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG","dwrite_3/DWRITE_FONT_PROPERTY_ID_FACE_NAME","dwrite_3/DWRITE_FONT_PROPERTY_ID_FAMILY_NAME","dwrite_3/DWRITE_FONT_PROPERTY_ID_FULL_NAME","dwrite_3/DWRITE_FONT_PROPERTY_ID_NONE","dwrite_3/DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME","dwrite_3/DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME","dwrite_3/DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG","dwrite_3/DWRITE_FONT_PROPERTY_ID_STRETCH","dwrite_3/DWRITE_FONT_PROPERTY_ID_STYLE","dwrite_3/DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG","dwrite_3/DWRITE_FONT_PROPERTY_ID_TOTAL","dwrite_3/DWRITE_FONT_PROPERTY_ID_WEIGHT","dwrite_3/DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME"]
old-location: directwrite\dwrite_font_property_id.htm
tech.root: DirectWrite
ms.assetid: 9743F54F-B661-444F-8579-DE03B0891F9C
ms.date: 09/10/2025
ms.keywords: DWRITE_FONT_PROPERTY_ID, DWRITE_FONT_PROPERTY_ID enumeration [Direct Write], DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG, DWRITE_FONT_PROPERTY_ID_FACE_NAME, DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, DWRITE_FONT_PROPERTY_ID_FULL_NAME, DWRITE_FONT_PROPERTY_ID_NONE, DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME, DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME, DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG, DWRITE_FONT_PROPERTY_ID_STRETCH, DWRITE_FONT_PROPERTY_ID_STYLE, DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG, DWRITE_FONT_PROPERTY_ID_TOTAL, DWRITE_FONT_PROPERTY_ID_WEIGHT, DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME, directwrite.dwrite_font_property_id, dwrite_3/DWRITE_FONT_PROPERTY_ID, dwrite_3/DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG, dwrite_3/DWRITE_FONT_PROPERTY_ID_FACE_NAME, dwrite_3/DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, dwrite_3/DWRITE_FONT_PROPERTY_ID_FULL_NAME, dwrite_3/DWRITE_FONT_PROPERTY_ID_NONE, dwrite_3/DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME, dwrite_3/DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME, dwrite_3/DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG, dwrite_3/DWRITE_FONT_PROPERTY_ID_STRETCH, dwrite_3/DWRITE_FONT_PROPERTY_ID_STYLE, dwrite_3/DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG, dwrite_3/DWRITE_FONT_PROPERTY_ID_TOTAL, dwrite_3/DWRITE_FONT_PROPERTY_ID_WEIGHT, dwrite_3/DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
ms.custom: 19H1
f1_keywords:
 - DWRITE_FONT_PROPERTY_ID
 - dwrite_3/DWRITE_FONT_PROPERTY_ID
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
 - DWRITE_FONT_PROPERTY_ID
---

# DWRITE_FONT_PROPERTY_ID enumeration


## -description

Identifies a string in a font.

## -enum-fields

### -field DWRITE_FONT_PROPERTY_ID_NONE

Unspecified font property identifier.

### -field DWRITE_FONT_PROPERTY_ID_WEIGHT_STRETCH_STYLE_FAMILY_NAME

### -field DWRITE_FONT_PROPERTY_ID_TYPOGRAPHIC_FAMILY_NAME

### -field DWRITE_FONT_PROPERTY_ID_WEIGHT_STRETCH_STYLE_FACE_NAME

### -field DWRITE_FONT_PROPERTY_ID_FULL_NAME

The full name of the font, for example "Arial Bold", from name id 4 in the name table.

### -field DWRITE_FONT_PROPERTY_ID_WIN32_FAMILY_NAME

GDI-compatible family name. Because GDI allows a maximum of four fonts per family, fonts in the same family may have different GDI-compatible family names,
          for example "Arial", "Arial Narrow", "Arial Black".

### -field DWRITE_FONT_PROPERTY_ID_POSTSCRIPT_NAME

The postscript name of the font, for example "GillSans-Bold", from name id 6 in the name table.

### -field DWRITE_FONT_PROPERTY_ID_DESIGN_SCRIPT_LANGUAGE_TAG

Script/language tag to identify the scripts or languages that the font was primarily designed to support.

### -field DWRITE_FONT_PROPERTY_ID_SUPPORTED_SCRIPT_LANGUAGE_TAG

Script/language tag to identify the scripts or languages that the font declares it is able to support.

### -field DWRITE_FONT_PROPERTY_ID_SEMANTIC_TAG

Semantic tag to describe the font, for example Fancy, Decorative, Handmade, Sans-serif, Swiss, Pixel, Futuristic.

### -field DWRITE_FONT_PROPERTY_ID_WEIGHT

Weight of the font represented as a decimal string in the range 1-999.

### -field DWRITE_FONT_PROPERTY_ID_STRETCH

Stretch of the font represented as a decimal string in the range 1-9.

### -field DWRITE_FONT_PROPERTY_ID_STYLE

Style of the font represented as a decimal string in the range 0-2.

### -field DWRITE_FONT_PROPERTY_ID_TYPOGRAPHIC_FACE_NAME

### -field DWRITE_FONT_PROPERTY_ID_TOTAL

Total number of properties.

### -field DWRITE_FONT_PROPERTY_ID_TOTAL_RS3

### -field DWRITE_FONT_PROPERTY_ID_PREFERRED_FAMILY_NAME

Family name preferred by the designer. This enables font designers to group more than four fonts in a single family without losing compatibility with
          GDI. This name is typically only present if it differs from the GDI-compatible family name.

### -field DWRITE_FONT_PROPERTY_ID_FAMILY_NAME

Family name for the weight-width-slope model.

### -field DWRITE_FONT_PROPERTY_ID_FACE_NAME

Face name of the font, for example Regular or Bold.

