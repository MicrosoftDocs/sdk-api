---
UID: NF:gdipluspen.Pen.GetCompoundArray
title: Pen::GetCompoundArray (gdipluspen.h)
description: The Pen::GetCompoundArray method gets the compound array currently set for this Pen object.
helpviewer_keywords: ["GetCompoundArray","GetCompoundArray method [GDI+]","GetCompoundArray method [GDI+]","Pen class","Pen class [GDI+]","GetCompoundArray method","Pen.GetCompoundArray","Pen::GetCompoundArray","_gdiplus_CLASS_Pen_GetCompoundArray_compoundArray_count_","gdiplus._gdiplus_CLASS_Pen_GetCompoundArray_compoundArray_count_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_GetCompoundArray_compoundArray_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\getcompoundarray.htm
ms.date: 12/05/2018
ms.keywords: GetCompoundArray, GetCompoundArray method [GDI+], GetCompoundArray method [GDI+],Pen class, Pen class [GDI+],GetCompoundArray method, Pen.GetCompoundArray, Pen::GetCompoundArray, _gdiplus_CLASS_Pen_GetCompoundArray_compoundArray_count_, gdiplus._gdiplus_CLASS_Pen_GetCompoundArray_compoundArray_count_
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
 - Pen::GetCompoundArray
 - gdipluspen/Pen::GetCompoundArray
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
 - Pen.GetCompoundArray
---

# Pen::GetCompoundArray


## -description

The <b>Pen::GetCompoundArray</b> method gets the compound array currently set for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param compoundArray [out]

Type: <b>REAL*</b>

Pointer to an array that receives the compound array.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>compoundArray</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Suppose that a compound array contains the values 0.0, 0.2, 0.7, and 1.0 and that the pen has a width of 100. When you use the pen to draw, you get two parallel lines. The first line has a width of 20, the space between the two lines has a width of 50, and the second line has a width of 30.

For a more complex example, suppose that a compound array contains the values 0.0, 0.2, 0.3, 0.6, 0.85, and 1.0 and that the pen has a width of 100. When you use the pen to draw, you get three parallel lines. The widths of the three lines are 20, 30, and 15 respectively. The widths of the two spaces between the lines are 10 and 25 respectively.


#### Examples



The following example gets the compound array for a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object. Assuming that a compound array has been set for this <b>Pen</b> object, the code then gets the entries that have been set for this pen.


```cpp
INT count = pen.GetCompoundCount();
REAL * distances = new REAL[count];
Status stat = pen.GetCompoundArray(distances, count);
```

## -see-also

<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-setcompoundarray">Pen::SetCompoundArray</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>