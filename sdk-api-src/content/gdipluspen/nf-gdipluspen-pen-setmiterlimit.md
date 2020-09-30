---
UID: NF:gdipluspen.Pen.SetMiterLimit
title: Pen::SetMiterLimit (gdipluspen.h)
description: The Pen::SetMiterLimit method sets the miter limit of this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetMiterLimit method","Pen.SetMiterLimit","Pen::SetMiterLimit","SetMiterLimit","SetMiterLimit method [GDI+]","SetMiterLimit method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_","gdiplus._gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setmiterlimit.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetMiterLimit method, Pen.SetMiterLimit, Pen::SetMiterLimit, SetMiterLimit, SetMiterLimit method [GDI+], SetMiterLimit method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_, gdiplus._gdiplus_CLASS_Pen_SetMiterLimit_miterLimit_
req.header: gdipluspen.h
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
 - Pen::SetMiterLimit
 - gdipluspen/Pen::SetMiterLimit
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
 - Pen.SetMiterLimit
---

# Pen::SetMiterLimit


## -description

The <b>Pen::SetMiterLimit</b> method sets the miter limit of this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param miterLimit [in]

Type: <b>REAL</b>

Real number that specifies the miter limit of this 
					<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. A real number value that is less than 1.0f will be replaced with 1.0f.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The miter length is the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls outside of the join. The miter length can be large when the angle between two lines is small. The miter limit is the maximum allowed ratio of miter length to stroke width. The default value is 10.0f.

If the miter length of the join of the intersection exceeds the limit of the join, then the join will be beveled to keep it within the limit of the join of the intersection.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object and sets the miter limit for the pen.


```cpp
Pen pen(Color(255,255,0,0), 4.0f);
Status stat = pen.SetMiterLimit(10.0f);
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-joining-lines-use">Joining Lines</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getmiterlimit">Pen::GetMiterLimit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>