---
UID: NE:dwrite.DWRITE_FONT_FILE_TYPE
title: DWRITE_FONT_FILE_TYPE (dwrite.h)
description: The type of a font represented by a single font file. Font formats that consist of multiple files, for example Type 1 .PFM and .PFB, have separate enum values for each of the file types.
helpviewer_keywords: ["DWRITE_FONT_FILE_TYPE","DWRITE_FONT_FILE_TYPE enumeration [Direct Write]","DWRITE_FONT_FILE_TYPE_BITMAP","DWRITE_FONT_FILE_TYPE_CFF","DWRITE_FONT_FILE_TYPE_TRUETYPE","DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION","DWRITE_FONT_FILE_TYPE_TYPE1_PFB","DWRITE_FONT_FILE_TYPE_TYPE1_PFM","DWRITE_FONT_FILE_TYPE_UNKNOWN","DWRITE_FONT_FILE_TYPE_VECTOR","directwrite.dwrite_font_file_type","dwrite/DWRITE_FONT_FILE_TYPE","dwrite/DWRITE_FONT_FILE_TYPE_BITMAP","dwrite/DWRITE_FONT_FILE_TYPE_CFF","dwrite/DWRITE_FONT_FILE_TYPE_TRUETYPE","dwrite/DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION","dwrite/DWRITE_FONT_FILE_TYPE_TYPE1_PFB","dwrite/DWRITE_FONT_FILE_TYPE_TYPE1_PFM","dwrite/DWRITE_FONT_FILE_TYPE_UNKNOWN","dwrite/DWRITE_FONT_FILE_TYPE_VECTOR"]
old-location: directwrite\dwrite_font_file_type.htm
tech.root: DirectWrite
ms.assetid: 04db41a6-b08b-4d01-a878-c05c0f1f2d9c
ms.date: 12/05/2018
ms.keywords: DWRITE_FONT_FILE_TYPE, DWRITE_FONT_FILE_TYPE enumeration [Direct Write], DWRITE_FONT_FILE_TYPE_BITMAP, DWRITE_FONT_FILE_TYPE_CFF, DWRITE_FONT_FILE_TYPE_TRUETYPE, DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION, DWRITE_FONT_FILE_TYPE_TYPE1_PFB, DWRITE_FONT_FILE_TYPE_TYPE1_PFM, DWRITE_FONT_FILE_TYPE_UNKNOWN, DWRITE_FONT_FILE_TYPE_VECTOR, directwrite.dwrite_font_file_type, dwrite/DWRITE_FONT_FILE_TYPE, dwrite/DWRITE_FONT_FILE_TYPE_BITMAP, dwrite/DWRITE_FONT_FILE_TYPE_CFF, dwrite/DWRITE_FONT_FILE_TYPE_TRUETYPE, dwrite/DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION, dwrite/DWRITE_FONT_FILE_TYPE_TYPE1_PFB, dwrite/DWRITE_FONT_FILE_TYPE_TYPE1_PFM, dwrite/DWRITE_FONT_FILE_TYPE_UNKNOWN, dwrite/DWRITE_FONT_FILE_TYPE_VECTOR
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
 - DWRITE_FONT_FILE_TYPE
 - dwrite/DWRITE_FONT_FILE_TYPE
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
 - DWRITE_FONT_FILE_TYPE
---

# DWRITE_FONT_FILE_TYPE enumeration


## -description

The type of a font represented by a single font file. Font formats that consist of multiple files, for example Type 1 .PFM and .PFB, have separate enum values for each of the file types.

## -enum-fields

### -field DWRITE_FONT_FILE_TYPE_UNKNOWN

Font type is not recognized by the DirectWrite font system.

### -field DWRITE_FONT_FILE_TYPE_CFF

OpenType font with CFF outlines.

### -field DWRITE_FONT_FILE_TYPE_TRUETYPE

OpenType font with TrueType outlines.

### -field DWRITE_FONT_FILE_TYPE_OPENTYPE_COLLECTION

### -field DWRITE_FONT_FILE_TYPE_TYPE1_PFM

Type 1 PFM font.

### -field DWRITE_FONT_FILE_TYPE_TYPE1_PFB

Type 1 PFB font.

### -field DWRITE_FONT_FILE_TYPE_VECTOR

Vector .FON font.

### -field DWRITE_FONT_FILE_TYPE_BITMAP

Bitmap .FON font.

### -field DWRITE_FONT_FILE_TYPE_TRUETYPE_COLLECTION

OpenType font that contains a TrueType collection.

