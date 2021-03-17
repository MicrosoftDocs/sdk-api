---
UID: NS:dwrite.DWRITE_STRIKETHROUGH
title: DWRITE_STRIKETHROUGH (dwrite.h)
description: Contains information regarding the size and placement of strikethroughs.
helpviewer_keywords: ["DWRITE_STRIKETHROUGH","DWRITE_STRIKETHROUGH structure [Direct Write]","directwrite.dwrite_strikethrough","dwrite/DWRITE_STRIKETHROUGH"]
old-location: directwrite\dwrite_strikethrough.htm
tech.root: DirectWrite
ms.assetid: 05d86485-2c34-4e3b-99e8-ca54a3b1e5f6
ms.date: 12/05/2018
ms.keywords: DWRITE_STRIKETHROUGH, DWRITE_STRIKETHROUGH structure [Direct Write], directwrite.dwrite_strikethrough, dwrite/DWRITE_STRIKETHROUGH
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
 - DWRITE_STRIKETHROUGH
 - dwrite/DWRITE_STRIKETHROUGH
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
 - DWRITE_STRIKETHROUGH
---

# DWRITE_STRIKETHROUGH structure


## -description

Contains information regarding the size and placement of strikethroughs.All coordinates are in device independent pixels (DIPs).

## -struct-fields

### -field width

Type: <b>FLOAT</b>

A value that indicates the width of the strikethrough, measured parallel to the baseline.

### -field thickness

Type: <b>FLOAT</b>

A value that indicates the thickness of the strikethrough, measured perpendicular to the baseline.

### -field offset

Type: <b>FLOAT</b>

A value that indicates the offset of the strikethrough from the baseline. 
	  A positive offset represents a position below the baseline and 
	  a negative offset is above.  Typically, the offset will be negative.

### -field readingDirection

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction">DWRITE_READING_DIRECTION</a></b>

Reading direction of the text associated with the strikethrough. 
	  This value is used to interpret whether the width value runs horizontally 
	  or vertically.

### -field flowDirection

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction">DWRITE_FLOW_DIRECTION</a></b>

Flow direction of the text associated with the strikethrough. 
	  This value is used to interpret whether the thickness value advances top to 
	  bottom, left to right, or right to left.

### -field localeName

Type: <b>const WCHAR*</b>

An array of characters containing the locale of the  text that is the strikethrough is being drawn over.

### -field measuringMode

Type: <b><a href="/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode">DWRITE_MEASURING_MODE</a></b>

The measuring mode can be useful to the renderer to determine how underlines are rendered, such as rounding the thickness to a whole pixel in GDI-compatible modes.

