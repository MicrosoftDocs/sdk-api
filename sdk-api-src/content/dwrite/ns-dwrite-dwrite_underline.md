---
UID: NS:dwrite.DWRITE_UNDERLINE
title: DWRITE_UNDERLINE
author: windows-sdk-content
description: Contains information about the width, thickness, offset, run height, reading direction, and flow direction of an underline.
old-location: directwrite\dwrite_underline.htm
tech.root: DirectWrite
ms.assetid: 01f6c48e-6986-4a6e-9dd8-9f4b098db7fd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWRITE_UNDERLINE, DWRITE_UNDERLINE structure [Direct Write], directwrite.dwrite_underline, dwrite/DWRITE_UNDERLINE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_UNDERLINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DWRITE_UNDERLINE structure


## -description


Contains information about the width, thickness, offset, run height, reading direction, and flow direction of an underline. 


## -struct-fields




### -field width

Type: <b>FLOAT</b>

A value that indicates the width of the underline, measured parallel to the baseline.


### -field thickness

Type: <b>FLOAT</b>

A value that indicates the thickness of the underline, measured perpendicular to the baseline.


### -field offset

Type: <b>FLOAT</b>

A value that indicates the offset of the underline from the baseline. A positive offset represents a position below the baseline (away from the text) and a negative offset is above (toward the text).


### -field runHeight

Type: <b>FLOAT</b>

A value that indicates the height of the tallest run where the underline is applied.


### -field readingDirection

Type: <b><a href="https://msdn.microsoft.com/37288d34-d533-474c-b3c0-8c6361074a9b">DWRITE_READING_DIRECTION</a></b>

A value that indicates the reading direction of the text associated with the underline. This value is used to interpret whether the width value runs horizontally or vertically.


### -field flowDirection

Type: <b><a href="https://msdn.microsoft.com/35a78bde-ba80-4328-8fb8-77ca73c1c04b">DWRITE_FLOW_DIRECTION</a></b>

A value that indicates the flow direction of the text associated with the underline. This value is used to interpret whether the thickness value advances top to bottom, left to right, or right to left.


### -field localeName

Type: <b>const WCHAR*</b>

An array of characters which contains the locale of the text that the underline is being drawn under.  For example, in vertical text, the underline belongs on the left for Chinese but on the right for Japanese. 


### -field measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring mode can be useful to the renderer to determine how underlines are rendered, such as rounding the thickness to a whole pixel in GDI-compatible modes.


## -remarks



All coordinates are in device independent pixels (DIPs).



