---
UID: NE:gdiplusenums.LineJoin
title: LineJoin (gdiplusenums.h)
description: The LineJoin enumeration specifies how to join two lines that are drawn by the same pen and whose ends meet. At the intersection of the two line ends, a line join makes the join look more continuous.
helpviewer_keywords: ["LineJoin","LineJoin enumeration [GDI+]","LineJoinBevel","LineJoinMiter","LineJoinMiterClipped","LineJoinRound","_gdiplus_ENUM_LineJoin","gdiplus._gdiplus_ENUM_LineJoin","gdiplusenums/LineJoin","gdiplusenums/LineJoinBevel","gdiplusenums/LineJoinMiter","gdiplusenums/LineJoinMiterClipped","gdiplusenums/LineJoinRound"]
old-location: gdiplus\_gdiplus_ENUM_LineJoin.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\linejoin.htm
ms.date: 12/05/2018
ms.keywords: LineJoin, LineJoin enumeration [GDI+], LineJoinBevel, LineJoinMiter, LineJoinMiterClipped, LineJoinRound, _gdiplus_ENUM_LineJoin, gdiplus._gdiplus_ENUM_LineJoin, gdiplusenums/LineJoin, gdiplusenums/LineJoinBevel, gdiplusenums/LineJoinMiter, gdiplusenums/LineJoinMiterClipped, gdiplusenums/LineJoinRound
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
 - LineJoin
 - gdiplusenums/LineJoin
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
 - LineJoin
---

# LineJoin enumeration


## -description

The <b>LineJoin</b> enumeration specifies how to join two lines that are drawn by the same pen and whose ends meet. At the intersection of the two line ends, a line join makes the join look more continuous.

## -enum-fields

### -field LineJoinMiter:0

Specifies a mitered join. This produces a sharp corner or a clipped corner, depending on whether the length of the miter exceeds the miter limit.

### -field LineJoinBevel:1

Specifies a beveled join. This produces a diagonal corner.

### -field LineJoinRound:2

Specifies a circular join. This produces a smooth, circular arc between the lines.

### -field LineJoinMiterClipped:3

Specifies a mitered join. This produces a sharp corner or a beveled corner, depending on whether the length of the miter exceeds the miter limit.

## -remarks

The miter length is the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls outside of the join. The miter length can be large when the angle between two lines is small. The miter limit is the maximum allowed ratio of miter length to stroke width. The default value is 10.0f.

When using <b><b>LineJoinMiter</b></b> and the actual ratio exceeds the miter limit, the corner is clipped perpendicular to the miter at a distance from the inner corner that is the product of the miter limit and the pen width. 

<img alt="Illustration showing two lines with a corner that is clipped: the outside walls of the lines do not meet at a point" src="./images/linejoinmiter.png"/>
When using <b><b>LineJoinMiterClipped</b></b> and the miter limit is exceeded, the join is drawn as if its type were <b><b>LineJoinBevel</b></b>; that is, when the line walls on the inside of the join meet, then a joining line is drawn between the line walls on the outside of the join.

<img alt="Illustration showing two lines with a corner that is beveled" src="./images/linejoinbevel.png"/>

## -see-also

<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setlinejoin">Pen::SetLineJoin</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setmiterlimit">Pen::SetMiterLimit</a>
