---
UID: NE:gdiplusenums.LineCap
title: LineCap
author: windows-sdk-content
description: The LineCap enumeration specifies the type of graphic shape to use on the end of a line drawn with a Windows GDI+ pen.
old-location: gdiplus\_gdiplus_ENUM_LineCap.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\linecap.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: LineCap, LineCap enumeration [GDI+], LineCapArrowAnchor, LineCapCustom, LineCapDiamondAnchor, LineCapFlat, LineCapNoAnchor, LineCapRound, LineCapRoundAnchor, LineCapSquare, LineCapSquareAnchor, LineCapTriangle, _gdiplus_ENUM_LineCap, gdiplus._gdiplus_ENUM_LineCap, gdiplusenums/LineCap, gdiplusenums/LineCapArrowAnchor, gdiplusenums/LineCapCustom, gdiplusenums/LineCapDiamondAnchor, gdiplusenums/LineCapFlat, gdiplusenums/LineCapNoAnchor, gdiplusenums/LineCapRound, gdiplusenums/LineCapRoundAnchor, gdiplusenums/LineCapSquare, gdiplusenums/LineCapSquareAnchor, gdiplusenums/LineCapTriangle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - LineCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LineCap enumeration


## -description


The <b>LineCap</b> enumeration specifies the type of graphic shape to use on the end of a line drawn with a Windows GDI+ pen. The cap can be a square, circle, triangle, arrowhead, custom, or masked (hidden). End caps can also "anchor" the line by centering the cap at the end of the line. 


## -enum-fields




### -field LineCapFlat

Specifies that the line ends at the last point. The end is squared off. 


### -field LineCapSquare

Specifies a square cap. The center of the square is the last point in the line. The height and width of the square are the line width. 


### -field LineCapRound

Specifies a circular cap. The center of the circle is the last point in the line. The diameter of the circle is the line width. 


### -field LineCapTriangle

Specifies a triangular cap. The base of the triangle is the last point in the line. The base of the triangle is the line width. 


### -field LineCapNoAnchor

Specifies that the line ends are not anchored. 


### -field LineCapSquareAnchor

Specifies that the line ends are anchored with a square. The center of the square is the last point in the line. The height and width of the square are the line width. 


### -field LineCapRoundAnchor

Specifies that the line ends are anchored with a circle. The center of the circle is at the last point in the line. The circle is wider than the line. 


### -field LineCapDiamondAnchor

Specifies that the line ends are anchored with a diamond (a square turned at 45 degrees). The center of the diamond is at the last point in the line. The diamond is wider than the line. 


### -field LineCapArrowAnchor

Specifies that the line ends are anchored with arrowheads. The arrowhead point is located at the last point in the line. The arrowhead is wider than the line. 


### -field LineCapCustom

Specifies that the line ends are made from a 
				<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>. 


### -field LineCapAnchorMask



