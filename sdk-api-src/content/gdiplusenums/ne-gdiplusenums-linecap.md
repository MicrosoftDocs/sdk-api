---
UID: NE:gdiplusenums.LineCap
title: LineCap (gdiplusenums.h)
description: The LineCap enumeration specifies the type of graphic shape to use on the end of a line drawn with a Windows GDI+ pen.
helpviewer_keywords: ["LineCap","LineCap enumeration [GDI+]","LineCapArrowAnchor","LineCapCustom","LineCapDiamondAnchor","LineCapFlat","LineCapNoAnchor","LineCapRound","LineCapRoundAnchor","LineCapSquare","LineCapSquareAnchor","LineCapTriangle","_gdiplus_ENUM_LineCap","gdiplus._gdiplus_ENUM_LineCap","gdiplusenums/LineCap","gdiplusenums/LineCapArrowAnchor","gdiplusenums/LineCapCustom","gdiplusenums/LineCapDiamondAnchor","gdiplusenums/LineCapFlat","gdiplusenums/LineCapNoAnchor","gdiplusenums/LineCapRound","gdiplusenums/LineCapRoundAnchor","gdiplusenums/LineCapSquare","gdiplusenums/LineCapSquareAnchor","gdiplusenums/LineCapTriangle"]
old-location: gdiplus\_gdiplus_ENUM_LineCap.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\linecap.htm
ms.date: 12/05/2018
ms.keywords: LineCap, LineCap enumeration [GDI+], LineCapArrowAnchor, LineCapCustom, LineCapDiamondAnchor, LineCapFlat, LineCapNoAnchor, LineCapRound, LineCapRoundAnchor, LineCapSquare, LineCapSquareAnchor, LineCapTriangle, _gdiplus_ENUM_LineCap, gdiplus._gdiplus_ENUM_LineCap, gdiplusenums/LineCap, gdiplusenums/LineCapArrowAnchor, gdiplusenums/LineCapCustom, gdiplusenums/LineCapDiamondAnchor, gdiplusenums/LineCapFlat, gdiplusenums/LineCapNoAnchor, gdiplusenums/LineCapRound, gdiplusenums/LineCapRoundAnchor, gdiplusenums/LineCapSquare, gdiplusenums/LineCapSquareAnchor, gdiplusenums/LineCapTriangle
req.header: gdiplusenums.h
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
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - LineCap
 - gdiplusenums/LineCap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - LineCap
---

# LineCap enumeration


## -description

The <b>LineCap</b> enumeration specifies the type of graphic shape to use on the end of a line drawn with a Windows GDI+ pen. The cap can be a square, circle, triangle, arrowhead, custom, or masked (hidden). End caps can also "anchor" the line by centering the cap at the end of the line.

## -enum-fields

### -field LineCapFlat:0

Specifies that the line ends at the last point. The end is squared off.

### -field LineCapSquare:1

Specifies a square cap. The center of the square is the last point in the line. The height and width of the square are the line width.

### -field LineCapRound:2

Specifies a circular cap. The center of the circle is the last point in the line. The diameter of the circle is the line width.

### -field LineCapTriangle:3

Specifies a triangular cap. The base of the triangle is the last point in the line. The base of the triangle is the line width.

### -field LineCapNoAnchor:0x10

Specifies that the line ends are not anchored.

### -field LineCapSquareAnchor:0x11

Specifies that the line ends are anchored with a square. The center of the square is the last point in the line. The height and width of the square are the line width.

### -field LineCapRoundAnchor:0x12

Specifies that the line ends are anchored with a circle. The center of the circle is at the last point in the line. The circle is wider than the line.

### -field LineCapDiamondAnchor:0x13

Specifies that the line ends are anchored with a diamond (a square turned at 45 degrees). The center of the diamond is at the last point in the line. The diamond is wider than the line.

### -field LineCapArrowAnchor:0x14

Specifies that the line ends are anchored with arrowheads. The arrowhead point is located at the last point in the line. The arrowhead is wider than the line.

### -field LineCapCustom:0xff

Specifies that the line ends are made from a 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-customlinecap">CustomLineCap</a>.

### -field LineCapAnchorMask:0xf0  
