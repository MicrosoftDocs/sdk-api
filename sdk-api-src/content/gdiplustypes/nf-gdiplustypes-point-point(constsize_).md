---
UID: NF:gdiplustypes.Point.Point(constSize&)
title: Point::Point(IN const Size &) (gdiplustypes.h)
description: Creates a Point object using a Size object to initialize the X and Y data members.
helpviewer_keywords: ["Point","Point class [GDI+]","Point constructor","Point constructor [GDI+]","Point constructor [GDI+]","Point class","Point.Point","Point.Point(IN const Size &)","Point.Point(const Size&)","Point::Point","Point::Point(IN const Size &)","_gdiplus_CLASS_Point_Point_size_","gdiplus._gdiplus_CLASS_Point_Point_size_"]
old-location: gdiplus\_gdiplus_CLASS_Point_Point_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pointclass\pointconstructors\point_95size.htm
ms.date: 12/05/2018
ms.keywords: Point, Point class [GDI+],Point constructor, Point constructor [GDI+], Point constructor [GDI+],Point class, Point.Point, Point.Point(IN const Size &), Point.Point(const Size&), Point::Point, Point::Point(IN const Size &), _gdiplus_CLASS_Point_Point_size_, gdiplus._gdiplus_CLASS_Point_Point_size_
req.header: gdiplustypes.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Point::Point
 - gdiplustypes/Point::Point
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Point.Point
---

# Point::Point(IN const Size &)


## -description

Creates a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object using a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members.

## -parameters

### -param size [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a></b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object whose 
					<b>Width</b> data member specifies the 
					<b>X</b> data member of this <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object, and whose 
					<b>Height</b> data member specifies the 
					<b>Y</b> data member of this <b>Point</b> object.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/gdiplus/-gdiplus-class-point-constructors">Point Constructors</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>