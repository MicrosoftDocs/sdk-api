---
UID: NF:gdiplustypes.Point.Equals
title: Point::Equals (gdiplustypes.h)
description: The Point::Equals method determines whether two Point objects are equal. Two points are considered equal if they have the same X and Y data members.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","Point class","Point class [GDI+]","Equals method","Point.Equals","Point::Equals","_gdiplus_CLASS_Point_Equals_point_","gdiplus._gdiplus_CLASS_Point_Equals_point_"]
old-location: gdiplus\_gdiplus_CLASS_Point_Equals_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pointclass\pointmethods\equals_4point.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Point class, Point class [GDI+],Equals method, Point.Equals, Point::Equals, _gdiplus_CLASS_Point_Equals_point_, gdiplus._gdiplus_CLASS_Point_Equals_point_
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
 - Point::Equals
 - gdiplustypes/Point::Equals
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
 - Point.Equals
---

# Point::Equals


## -description

The <b>Point::Equals</b> method determines whether two 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

## -parameters

### -param point [in]

Type: <b>const Point&amp;</b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that is compared to this 
					<b>Point</b> object.

## -returns

Type: <b>BOOL</b>

If the 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> objects are equal, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/previous-versions/ms535008(v=vs.85)">Point::operator+</a>



<a href="/previous-versions/ms535009(v=vs.85)">Point::operator-</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>