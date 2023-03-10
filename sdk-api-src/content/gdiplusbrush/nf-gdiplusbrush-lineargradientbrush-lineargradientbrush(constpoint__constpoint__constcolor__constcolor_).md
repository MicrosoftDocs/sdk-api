---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(constPoint&,constPoint&,constColor&,constColor&)
title: LinearGradientBrush::LinearGradientBrush(IN const Point &,IN const Point &,IN const Color &,IN const Color &) (gdiplusbrush.h)
description: This topic lists the constructors of the LinearGradientBrush class. For a complete class listing, see LinearGradientBrush Class. (overload 1/2)
helpviewer_keywords: ["LinearGradientBrush","LinearGradientBrush constructors [GDI+]","LinearGradientBrush.LinearGradientBrush","LinearGradientBrush.LinearGradientBrush(IN const Point &","IN const Point &","IN const Color &","IN const Color &)","LinearGradientBrush::LinearGradientBrush","LinearGradientBrush::LinearGradientBrush(IN const Point &","IN const Point &","IN const Color &","IN const Color &)","_gdiplus_CLASS_LinearGradientBrush_Constructors","gdiplus._gdiplus_CLASS_LinearGradientBrush_Constructors","gdiplusbrush/LinearGradientBrush"]
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_Constructors.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors.htm
ms.date: 12/05/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush constructors [GDI+], LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const Point &,IN const Point &,IN const Color &,IN const Color &), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const Point &,IN const Point &,IN const Color &,IN const Color &), _gdiplus_CLASS_LinearGradientBrush_Constructors, gdiplus._gdiplus_CLASS_LinearGradientBrush_Constructors, gdiplusbrush/LinearGradientBrush
req.header: gdiplusbrush.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - LinearGradientBrush::LinearGradientBrush
 - gdiplusbrush/LinearGradientBrush::LinearGradientBrush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - gdiplusbrush.h
api_name:
 - LinearGradientBrush.LinearGradientBrush
---

## -description

Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object from a set of boundary points and boundary colors.

## -parameters

### -param point1 [in, ref]

Type: <b>const <a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a **Point** object that specifies the starting point of the gradient. The starting boundary line passes through the starting point.

### -param point2 [in, ref]

Type: <b>const <a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-point">Point</a></b>

Reference to a **Point** object that specifies the ending point of the gradient. The ending boundary line passes through the ending point.

### -param color1 [in, ref]

Type: <b>const <a href="/windows/win32/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/win32/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush.

### -param color2 [in, ref]

Type: <b>const <a href="/windows/win32/api/gdipluscolor/nl-gdipluscolor-color">Color</a></b>

Reference to a <a href="/windows/win32/api/gdipluscolor/nl-gdipluscolor-color">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush.

## -remarks

The "directional line," an imaginary straight line, is defined by the starting point, <i>point1</i>, and the ending point, <i>point2</i>. The starting boundary of the gradient is a straight line that is perpendicular to the directional line and that passes through the starting point. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that passes through the ending point. The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line.

## -see-also

<a href="/windows/win32/api/gdipluscolor/nl-gdipluscolor-color">Color</a>


<a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-point">Point</a>


<a href="/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>

