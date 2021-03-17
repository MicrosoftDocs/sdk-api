---
UID: NE:dwrite.DWRITE_FONT_FACE_TYPE
title: DWRITE_FONT_FACE_TYPE (dwrite.h)
description: Indicates the file format of a complete font face.
helpviewer_keywords: ["DWRITE_FONT_FACE_TYPE","DWRITE_FONT_FACE_TYPE enumeration [Direct Write]","DWRITE_FONT_FACE_TYPE_BITMAP","DWRITE_FONT_FACE_TYPE_CFF","DWRITE_FONT_FACE_TYPE_RAW_CFF","DWRITE_FONT_FACE_TYPE_TRUETYPE","DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION","DWRITE_FONT_FACE_TYPE_TYPE1","DWRITE_FONT_FACE_TYPE_UNKNOWN","DWRITE_FONT_FACE_TYPE_VECTOR","directwrite.dwrite_font_face_type","dwrite/DWRITE_FONT_FACE_TYPE","dwrite/DWRITE_FONT_FACE_TYPE_BITMAP","dwrite/DWRITE_FONT_FACE_TYPE_CFF","dwrite/DWRITE_FONT_FACE_TYPE_RAW_CFF","dwrite/DWRITE_FONT_FACE_TYPE_TRUETYPE","dwrite/DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION","dwrite/DWRITE_FONT_FACE_TYPE_TYPE1","dwrite/DWRITE_FONT_FACE_TYPE_UNKNOWN","dwrite/DWRITE_FONT_FACE_TYPE_VECTOR"]
old-location: directwrite\dwrite_font_face_type.htm
tech.root: DirectWrite
ms.assetid: 839527fb-2560-4472-8115-960bf5b6badd
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_FACE_TYPE, DWRITE_FONT_FACE_TYPE enumeration [Direct Write], DWRITE_FONT_FACE_TYPE_BITMAP, DWRITE_FONT_FACE_TYPE_CFF, DWRITE_FONT_FACE_TYPE_RAW_CFF, DWRITE_FONT_FACE_TYPE_TRUETYPE, DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION, DWRITE_FONT_FACE_TYPE_TYPE1, DWRITE_FONT_FACE_TYPE_UNKNOWN, DWRITE_FONT_FACE_TYPE_VECTOR, directwrite.dwrite_font_face_type, dwrite/DWRITE_FONT_FACE_TYPE, dwrite/DWRITE_FONT_FACE_TYPE_BITMAP, dwrite/DWRITE_FONT_FACE_TYPE_CFF, dwrite/DWRITE_FONT_FACE_TYPE_RAW_CFF, dwrite/DWRITE_FONT_FACE_TYPE_TRUETYPE, dwrite/DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION, dwrite/DWRITE_FONT_FACE_TYPE_TYPE1, dwrite/DWRITE_FONT_FACE_TYPE_UNKNOWN, dwrite/DWRITE_FONT_FACE_TYPE_VECTOR
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_FONT_FACE_TYPE
 - dwrite/DWRITE_FONT_FACE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_FONT_FACE_TYPE
---

# DWRITE_FONT_FACE_TYPE enumeration


## -description

Indicates the file format of a complete font face.

## -enum-fields

### -field DWRITE_FONT_FACE_TYPE_CFF

OpenType font face with CFF outlines.

### -field DWRITE_FONT_FACE_TYPE_TRUETYPE

OpenType font face with TrueType outlines.

### -field DWRITE_FONT_FACE_TYPE_OPENTYPE_COLLECTION

### -field DWRITE_FONT_FACE_TYPE_TYPE1

A Type 1 font face.

### -field DWRITE_FONT_FACE_TYPE_VECTOR

A vector .FON format font face.

### -field DWRITE_FONT_FACE_TYPE_BITMAP

A bitmap .FON format font face.

### -field DWRITE_FONT_FACE_TYPE_UNKNOWN

Font face type is not recognized by the DirectWrite font system.

### -field DWRITE_FONT_FACE_TYPE_RAW_CFF

The font data includes only the CFF table from an OpenType CFF font. This font face type can be used only for embedded fonts (i.e., custom font file loaders) and the resulting font face object supports only the minimum functionality necessary to render glyphs.

### -field DWRITE_FONT_FACE_TYPE_TRUETYPE_COLLECTION

OpenType font face that is a part of a TrueType collection.

## -remarks

Font formats that consist of multiple files, such as Type 1 .PFM and .PFB, have a single enum entry.

