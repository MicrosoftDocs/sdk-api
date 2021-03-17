---
UID: NS:olectl.tagPICTDESC
title: PICTDESC (olectl.h)
description: Contains parameters to create a picture object through the OleCreatePictureIndirect function.
helpviewer_keywords: ["*LPPICTDESC","LPPICTDESC","LPPICTDESC structure pointer [COM]","PICTDESC","PICTDESC structure [COM]","_ctrl_PICTDESC","com.pictdesc","olectl/LPPICTDESC","olectl/PICTDESC"]
old-location: com\pictdesc.htm
tech.root: com
ms.assetid: eb1f1de7-dcfe-4c1c-8737-f5ab4d7977d6
ms.date: 12/05/2018
ms.keywords: '*LPPICTDESC, LPPICTDESC, LPPICTDESC structure pointer [COM], PICTDESC, PICTDESC structure [COM], _ctrl_PICTDESC, com.pictdesc, olectl/LPPICTDESC, olectl/PICTDESC'
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PICTDESC, *LPPICTDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPICTDESC
 - olectl/tagPICTDESC
 - LPPICTDESC
 - olectl/LPPICTDESC
 - PICTDESC
 - olectl/PICTDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Olectl.h
api_name:
 - PICTDESC
---

# PICTDESC structure


## -description

Contains parameters to create a picture object through the <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a> function.

## -struct-fields

### -field cbSizeofstruct

The size of the structure, in bytes.

### -field picType

Type of picture described by this structure, which can be any value from the <a href="/windows/desktop/com/pictype-constants">PICTYPE</a> enumeration. This selects the arm of the union that corresponds to one of the picture type structures below.

### -field bmp

Structure containing bitmap information if <b>picType</b> is <b>PICTYPE_BITMAP</b>.

### -field bmp.hbitmap

The <b>HBITMAP</b> handle identifying the bitmap assigned to the picture object.

### -field bmp.hpal

The <b>HPALETTE</b> handle identifying the color palette for the bitmap.

### -field wmf

Structure containing metafile information if <b>picType</b> is <b>PICTYPE_METAFILE</b>.

### -field wmf.hmeta

The <b>HMETAFILE</b> handle identifying the metafile assigned to the picture object.

### -field wmf.xExt

Horizontal extent of the metafile in TWIPS units.

### -field wmf.yExt

Vertical extent of the metafile in TWIPS units.

### -field icon

Identifies a structure containing icon information if <b>picType</b> is <b>PICTYPE_ICON</b>.

### -field icon.hicon

The <b>HICON</b> handle identifying the icon assigned to the picture object.

### -field emf

Structure containing enhanced metafile information if <b>picType</b> is <b>PICTYPE_ENHMETAFILE</b>.

### -field emf.hemf

The <b>HENHMETAFILE</b> handle identifying the enhanced metafile assigned to the picture object.

## -see-also

<a href="/windows/desktop/api/olectl/nf-olectl-olecreatepictureindirect">OleCreatePictureIndirect</a>



<a href="/windows/desktop/com/pictype-constants">PICTYPE</a>