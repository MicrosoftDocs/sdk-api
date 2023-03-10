---
UID: NF:gdiplustypes.PointF.Equals
title: PointF::Equals (gdiplustypes.h)
description: The PointF::Equals method determines whether two PointF objects are equal. Two points are considered equal if they have the same X and Y data members.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","PointF class","PointF class [GDI+]","Equals method","PointF.Equals","PointF::Equals","_gdiplus_CLASS_PointF_Equals_point_","gdiplus._gdiplus_CLASS_PointF_Equals_point_"]
old-location: gdiplus\_gdiplus_CLASS_PointF_Equals_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pointfclass\pointfmethods\equals_39point.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],PointF class, PointF class [GDI+],Equals method, PointF.Equals, PointF::Equals, _gdiplus_CLASS_PointF_Equals_point_, gdiplus._gdiplus_CLASS_PointF_Equals_point_
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
 - PointF::Equals
 - gdiplustypes/PointF::Equals
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
 - PointF.Equals
---

# PointF::Equals


## -description

The <b>PointF::Equals</b> method determines whether two 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

## -parameters

### -param point [in]

Type: <b>const PointF&amp;</b>

Reference to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object that is compared to this 
					<b>PointF</b> object.

## -returns

Type: <b>BOOL</b>

If the 
						<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> objects are equal, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>



<a href="/previous-versions/ms534997(v=vs.85)">PointF::operator+</a>



<a href="/previous-versions/ms534998(v=vs.85)">PointF::operator-</a>