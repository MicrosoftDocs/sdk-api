---
UID: NF:gdipluspen.Pen.GetDashOffset
title: Pen::GetDashOffset (gdipluspen.h)
description: The Pen::GetDashOffset method gets the distance from the start of the line to the start of the first space in a dashed line.
helpviewer_keywords: ["GetDashOffset","GetDashOffset method [GDI+]","GetDashOffset method [GDI+]","Pen class","Pen class [GDI+]","GetDashOffset method","Pen.GetDashOffset","Pen::GetDashOffset","_gdiplus_CLASS_Pen_GetDashOffset_","gdiplus._gdiplus_CLASS_Pen_GetDashOffset_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetDashOffset_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getdashoffset.htm
ms.date: 12/05/2018
ms.keywords: GetDashOffset, GetDashOffset method [GDI+], GetDashOffset method [GDI+],Pen class, Pen class [GDI+],GetDashOffset method, Pen.GetDashOffset, Pen::GetDashOffset, _gdiplus_CLASS_Pen_GetDashOffset_, gdiplus._gdiplus_CLASS_Pen_GetDashOffset_
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
 - Pen::GetDashOffset
 - gdipluspen/Pen::GetDashOffset
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
 - Pen.GetDashOffset
---

# Pen::GetDashOffset


## -description

The <b>Pen::GetDashOffset</b> method gets the distance from the start of the line to the start of the first space in a dashed line.



## -returns

Type: <b>REAL</b>

This method returns a real number that indicates the distance from the start of the line to the start of the dashes.

## -remarks

A positive return value shifts the first dash forward along the path, and a negative return value shifts the start of the path forward along the first dash. 


#### Examples



The following example assumes that 
						<i>dashPen</i> has been defined with a certain dash style and gets the dash offset value.


```cpp
REAL dashOffset = dashPen.GetDashOffset();
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setdashoffset">Pen::SetDashOffset</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>
