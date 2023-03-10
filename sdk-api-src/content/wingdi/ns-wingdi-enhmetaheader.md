---
UID: NS:wingdi.tagENHMETAHEADER
title: ENHMETAHEADER (wingdi.h)
description: The ENHMETAHEADER structure contains enhanced-metafile data such as the dimensions of the picture stored in the enhanced metafile, the count of records in the enhanced metafile, the resolution of the device on which the picture was created, and so on.This structure is always the first record in an enhanced metafile.
helpviewer_keywords: ["*LPENHMETAHEADER","*PENHMETAHEADER","ENHMETAHEADER","ENHMETAHEADER structure [Windows GDI]","PENHMETAHEADER","PENHMETAHEADER structure pointer [Windows GDI]","_win32_ENHMETAHEADER_str","gdi.enhmetaheader","wingdi/ENHMETAHEADER","wingdi/PENHMETAHEADER"]
old-location: gdi\enhmetaheader.htm
tech.root: gdi
ms.assetid: 8e5f9a51-a995-48be-b936-1766fccb603a
ms.date: 12/05/2018
ms.keywords: '*LPENHMETAHEADER, *PENHMETAHEADER, ENHMETAHEADER, ENHMETAHEADER structure [Windows GDI], PENHMETAHEADER, PENHMETAHEADER structure pointer [Windows GDI], _win32_ENHMETAHEADER_str, gdi.enhmetaheader, wingdi/ENHMETAHEADER, wingdi/PENHMETAHEADER'
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
req.typenames: ENHMETAHEADER, *PENHMETAHEADER, *LPENHMETAHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagENHMETAHEADER
 - wingdi/tagENHMETAHEADER
 - PENHMETAHEADER
 - wingdi/PENHMETAHEADER
 - ENHMETAHEADER
 - wingdi/ENHMETAHEADER
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
 - ENHMETAHEADER
---

# ENHMETAHEADER structure


## -description

The <b>ENHMETAHEADER</b> structure contains enhanced-metafile data such as the dimensions of the picture stored in the enhanced metafile, 
		  the count of records in the enhanced metafile, the resolution of the device on which the picture was created, and so on.

This structure is always the first record in an enhanced
        metafile.

## -struct-fields

### -field iType

The record type. This member must specify the value assigned to the EMR_HEADER constant.

### -field nSize

The structure size, in bytes.

### -field rclBounds

The dimensions, in device units, of the smallest rectangle that can be drawn around the picture stored in the metafile. 
			 This rectangle is supplied by graphics device interface (GDI). Its dimensions include the right and bottom edges.

### -field rclFrame

The dimensions, in .01 millimeter units, of a rectangle that surrounds the picture stored in the metafile. 
			 This rectangle must be supplied by the application that creates the metafile. Its dimensions include the right and bottom edges.

### -field dSignature

A signature. This member must specify the value assigned to the ENHMETA_SIGNATURE constant.

### -field nVersion

The metafile version. The current version value is 0x10000.

### -field nBytes

The size of the enhanced metafile, in bytes.

### -field nRecords

The number of records in the enhanced metafile.

### -field nHandles

The number of handles in the enhanced-metafile handle table. (Index zero in this table is reserved.)

### -field sReserved

Reserved; must be zero.

### -field nDescription

The number of characters in the array that contains the description of the enhanced metafile's contents. 
			 This member should be set to zero if the enhanced metafile does not contain a description string.

### -field offDescription

The offset from the beginning of the <b>ENHMETAHEADER</b> structure to the array that contains the description of the enhanced metafile's contents. 
			 This member should be set to zero if the enhanced metafile does not contain a description string.

### -field nPalEntries

The number of entries in the enhanced metafile's palette.

### -field szlDevice

The resolution of the reference device, in pixels.

### -field szlMillimeters

The resolution of the reference device, in millimeters.

### -field cbPixelFormat

The size of the last recorded pixel format in a metafile. 
	 If a pixel format is set in a reference DC at the start of recording, <i>cbPixelFormat</i> is set to the size of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a>. 
	 When no pixel format is set when a metafile is recorded, this member is set to zero. 
	 If more than a single pixel format is set, the header points to the last pixel format.

### -field offPixelFormat

The offset of pixel format used when recording a metafile. 
	 If a pixel format is set in a reference DC at the start of recording or during recording, 
	 <i>offPixelFormat</i> is set to the offset of the <a href="/windows/desktop/api/wingdi/ns-wingdi-pixelformatdescriptor">PIXELFORMATDESCRIPTOR</a> in the metafile. 
	 If no pixel format is set when a metafile is recorded, this member is set to zero. 
	 If more than a single pixel format is set, the header points to the last pixel format.

### -field bOpenGL

Indicates whether any OpenGL records are present in a metafile. 
	 <i>bOpenGL</i> is a simple Boolean flag that you can use to determine whether an enhanced metafile requires OpenGL handling. 
	 When a metafile contains OpenGL records, <i>bOpenGL</i> is <b>TRUE</b>; otherwise it is <b>FALSE</b>.

### -field szlMicrometers

The size of the reference device, in micrometers.

## -see-also

<a href="/windows/desktop/api/wingdi/ns-wingdi-enhmetarecord">ENHMETARECORD</a>



<a href="/windows/desktop/gdi/metafile-structures">Metafile Structures</a>



<a href="/windows/desktop/gdi/metafiles">Metafiles Overview</a>



<a href="/windows/win32/api/windef/ns-windef-rectl">RECTL</a>