---
UID: NS:gdiplusmetaheader.ENHMETAHEADER3
title: ENHMETAHEADER3 (gdiplusmetaheader.h)
description: The ENHMETAHEADER3 structure contains enhanced-metafile data including the dimensions of the metafile image, the number of records in the metafile, and the resolution of the device on which the metafile was created.
helpviewer_keywords: ["ENHMETAHEADER3","ENHMETAHEADER3 structure [GDI+]","_gdiplus_STRUC_ENHMETAHEADER3","gdiplus._gdiplus_STRUC_ENHMETAHEADER3","gdiplusmetaheader/ENHMETAHEADER3"]
old-location: gdiplus\_gdiplus_STRUC_ENHMETAHEADER3.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\enhmetaheader3.htm
ms.date: 12/05/2018
ms.keywords: ENHMETAHEADER3, ENHMETAHEADER3 structure [GDI+], _gdiplus_STRUC_ENHMETAHEADER3, gdiplus._gdiplus_STRUC_ENHMETAHEADER3, gdiplusmetaheader/ENHMETAHEADER3
req.header: gdiplusmetaheader.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: ENHMETAHEADER3
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ENHMETAHEADER3
 - gdiplusmetaheader/ENHMETAHEADER3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusmetaheader.h
api_name:
 - ENHMETAHEADER3
---

# ENHMETAHEADER3 structure


## -description

The <b>ENHMETAHEADER3</b> structure contains enhanced-metafile data including the dimensions of the metafile image, the number of records in the metafile, and the resolution of the device on which the metafile was created.

## -struct-fields

### -field iType

Type: <b>DWORD</b>

Record type. Value is always EMR_HEADER.

### -field nSize

Type: <b>DWORD</b>

Structure size, in bytes. This may be greater than the value returned by <b>sizeof</b>(<b>ENHMETAHEADER3</b>).

### -field rclBounds

Type: <b>RECTL</b>

Bounding rectangle, in device units, for the image stored in the metafile.

### -field rclFrame

Type: <b>RECTL</b>

Rectangle, in 0.01 millimeter units, that surrounds the image stored in the metafile.

### -field dSignature

Type: <b>DWORD</b>

Must be ENHMETA_SIGNATURE.

### -field nVersion

Type: <b>DWORD</b>

Version number of the metafile format. The current version is 0x10000.

### -field nBytes

Type: <b>DWORD</b>

Size, in bytes, of the metafile.

### -field nRecords

Type: <b>DWORD</b>

Number of records in the metafile.

### -field nHandles

Type: <b>WORD</b>

Number of handles in the metafile handle table. Handle index zero is reserved.

### -field sReserved

Type: <b>WORD</b>

Reserved. Must be zero.

### -field nDescription

Type: <b>DWORD</b>

Number of characters in the string that contains the description of the metafile's contents. This member is 0 if the metafile does not have a description string.

### -field offDescription

Type: <b>DWORD</b>

Offset from the beginning of the <b>ENHMETAHEADER3</b> structure to the string that contains the description of the metafile's contents. This member is 0 if the metafile does not have a description string.

### -field nPalEntries

Type: <b>DWORD</b>

Number of entries in the metafile palette.

### -field szlDevice

Type: <b>SIZEL</b>

Resolution, in pixels, of the reference device.

### -field szlMillimeters

Type: <b>SIZEL</b>

Resolution, in millimeters, of the reference device.

