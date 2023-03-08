---
UID: NF:gdipluspen.Pen.GetMiterLimit
title: Pen::GetMiterLimit (gdipluspen.h)
description: The Pen::GetMiterLimit method gets the miter length currently set for this Pen object.
helpviewer_keywords: ["GetMiterLimit","GetMiterLimit method [GDI+]","GetMiterLimit method [GDI+]","Pen class","Pen class [GDI+]","GetMiterLimit method","Pen.GetMiterLimit","Pen::GetMiterLimit","_gdiplus_CLASS_Pen_GetMiterLimit_","gdiplus._gdiplus_CLASS_Pen_GetMiterLimit_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetMiterLimit_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getmiterlimit.htm
ms.date: 12/05/2018
ms.keywords: GetMiterLimit, GetMiterLimit method [GDI+], GetMiterLimit method [GDI+],Pen class, Pen class [GDI+],GetMiterLimit method, Pen.GetMiterLimit, Pen::GetMiterLimit, _gdiplus_CLASS_Pen_GetMiterLimit_, gdiplus._gdiplus_CLASS_Pen_GetMiterLimit_
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
 - Pen::GetMiterLimit
 - gdipluspen/Pen::GetMiterLimit
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
 - Pen.GetMiterLimit
---

# Pen::GetMiterLimit


## -description

The <b>Pen::GetMiterLimit</b> method gets the miter length currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.



## -returns

Type: <b>REAL</b>

This method returns a real number that indicates the miter limit of this 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -remarks

The miter length is the distance from the intersection of the line walls on the inside of the join to the intersection of the line walls outside of the join. The miter length can be large when the angle between two lines is small. The miter limit is the maximum allowed ratio of miter length to line width. The default value is 10.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object and gets the miter limit.


```cpp
Pen pen(Color(255,255,0,0), 4.0f);
REAL miterLimit = pen.GetMiterLimit(); 
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-joining-lines-use">Joining Lines</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setmiterlimit">Pen::SetMiterLimit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
