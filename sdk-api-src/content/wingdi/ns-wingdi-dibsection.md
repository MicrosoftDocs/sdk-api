---
UID: NS:wingdi.tagDIBSECTION
title: DIBSECTION (wingdi.h)
description: The DIBSECTION structure contains information about a DIB created by calling the CreateDIBSection function.
helpviewer_keywords: ["*LPDIBSECTION","*PDIBSECTION","DIBSECTION","DIBSECTION structure [Windows GDI]","PDIBSECTION","PDIBSECTION structure pointer [Windows GDI]","_win32_DIBSECTION_str","gdi.dibsection","wingdi/DIBSECTION","wingdi/PDIBSECTION"]
old-location: gdi\dibsection.htm
tech.root: gdi
ms.assetid: 76e84c90-6553-46c6-9ab9-afa022e0b2e5
ms.date: 12/05/2018
ms.keywords: '*LPDIBSECTION, *PDIBSECTION, DIBSECTION, DIBSECTION structure [Windows GDI], PDIBSECTION, PDIBSECTION structure pointer [Windows GDI], _win32_DIBSECTION_str, gdi.dibsection, wingdi/DIBSECTION, wingdi/PDIBSECTION'
req.header: wingdi.h
req.include-header: Windows.h
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
req.typenames: DIBSECTION, *LPDIBSECTION, *PDIBSECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDIBSECTION
 - wingdi/tagDIBSECTION
 - LPDIBSECTION
 - wingdi/LPDIBSECTION
 - DIBSECTION
 - wingdi/DIBSECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wingdi.h
api_name:
 - DIBSECTION
---

# DIBSECTION structure


## -description

The <b>DIBSECTION</b> structure contains information about a DIB created by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function. A <b>DIBSECTION</b> structure includes information about the bitmap's dimensions, color format, color masks, optional file mapping object, and optional bit values storage offset. An application can obtain a filled-in <b>DIBSECTION</b> structure for a given DIB by calling the <a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a> function.

## -struct-fields

### -field dsBm

A <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a> data structure that contains information about the DIB: its type, its dimensions, its color capacities, and a pointer to its bit values.

### -field dsBmih

A <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains information about the color format of the DIB.

### -field dsBitfields

Specifies three color masks for the DIB. This field is only valid when the <b>BitCount</b> member of the <a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure has a value greater than 8. Each color mask indicates the bits that are used to encode one of the three color channels (red, green, and blue).

### -field dshSection

Contains a handle to the file mapping object that the <a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a> function used to create the DIB. 
			 If <b>CreateDIBSection</b> was called with a <b>NULL</b> value for its <i>hSection</i> parameter, 
			 causing the system to allocate memory for the bitmap, the <i>dshSection</i> member will be <b>NULL</b>.

### -field dsOffset

The offset to the bitmap's bit values within the file mapping object referenced by <i>dshSection</i>. 
			 If <i>dshSection</i> is <b>NULL</b>, the <i>dsOffset</i> value has no meaning.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmap">BITMAP</a>



<a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a>



<a href="/windows/desktop/gdi/bitmap-structures">Bitmap Structures</a>



<a href="/windows/desktop/gdi/bitmaps">Bitmaps Overview</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-createdibsection">CreateDIBSection</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getdibcolortable">GetDIBColorTable</a>



<a href="/windows/desktop/api/wingdi/nf-wingdi-getobject">GetObject</a>