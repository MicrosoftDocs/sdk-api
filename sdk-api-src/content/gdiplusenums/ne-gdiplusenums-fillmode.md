---
UID: NE:gdiplusenums.FillMode
title: FillMode (gdiplusenums.h)
description: The FillMode enumeration specifies how to fill areas that are formed when a path or curve intersects itself.
helpviewer_keywords: ["FillMode","FillMode enumeration [GDI+]","FillModeAlternate","FillModeWinding","_gdiplus_ENUM_FillMode","gdiplus._gdiplus_ENUM_FillMode","gdiplusenums/FillMode","gdiplusenums/FillModeAlternate","gdiplusenums/FillModeWinding"]
old-location: gdiplus\_gdiplus_ENUM_FillMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\fillmode.htm
ms.date: 12/05/2018
ms.keywords: FillMode, FillMode enumeration [GDI+], FillModeAlternate, FillModeWinding, _gdiplus_ENUM_FillMode, gdiplus._gdiplus_ENUM_FillMode, gdiplusenums/FillMode, gdiplusenums/FillModeAlternate, gdiplusenums/FillModeWinding
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
 - FillMode
 - gdiplusenums/FillMode
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
 - FillMode
---

# FillMode enumeration


## -description

The <b>FillMode</b> enumeration specifies how to fill areas that are formed when a path or curve intersects itself. This enumeration is used by several methods of the <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> class, including 
			<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal)">FillClosedCurve</a> and 
			<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpointf_inint_infillmode)">FillPolygon</a>, and by the constructors of the 
			<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> class.

## -enum-fields

### -field FillModeAlternate

Specifies that areas are filled according to the even-odd parity rule. According to this rule, you can determine whether a test point is inside or outside a closed curve as follows: Draw a line from the test point to a point that is distant from the curve. If that line crosses the curve an odd number of times, the test point is inside the curve; otherwise, the test point is outside the curve.

### -field FillModeWinding

Specifies that areas are filled according to the nonzero winding rule. According to this rule, you can determine whether a test point is inside or outside a closed curve as follows: Draw a line from a test point to a point that is distant from the curve. Count the number of times the curve crosses the test line from left to right, and count the number of times the curve crosses the test line from right to left. If those two numbers are the same, the test point is outside the curve; otherwise, the test point is inside the curve.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillclosedcurve(inconstbrush_inconstpointf_inint_infillmode_inreal)">FillClosedCurve Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpolygon(inconstbrush_inconstpointf_inint_infillmode)">FillPolygon Methods</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-graphicspath(constgraphicspath_)">GraphicsPath Constructors</a>