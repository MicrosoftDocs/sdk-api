---
UID: NF:gdipluspen.Pen.SetCompoundArray
title: Pen::SetCompoundArray (gdipluspen.h)
description: The Pen::SetCompoundArray method sets the compound array for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetCompoundArray method","Pen.SetCompoundArray","Pen::SetCompoundArray","SetCompoundArray","SetCompoundArray method [GDI+]","SetCompoundArray method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetCompoundArray_compoundArray_count_","gdiplus._gdiplus_CLASS_Pen_SetCompoundArray_compoundArray_count_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetCompoundArray_compoundArray_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setcompoundarray.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetCompoundArray method, Pen.SetCompoundArray, Pen::SetCompoundArray, SetCompoundArray, SetCompoundArray method [GDI+], SetCompoundArray method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetCompoundArray_compoundArray_count_, gdiplus._gdiplus_CLASS_Pen_SetCompoundArray_compoundArray_count_
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
 - Pen::SetCompoundArray
 - gdipluspen/Pen::SetCompoundArray
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
 - Pen.SetCompoundArray
---

# Pen::SetCompoundArray


## -description

The <b>Pen::SetCompoundArray</b> method sets the compound array for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param compoundArray [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specifies the compound array. The elements in the array must be in increasing order, not less than 0, and not greater than 1.

### -param count [in]

Type: <b>INT</b>

Positive even integer that specifies the number of elements in the 
					<i>compoundArray</i> array. The integer must not be greater than the number of elements in the compound array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

Suppose you want a pen to draw two parallel lines where the width of the first line is 20 percent of the pen's width, the width of the space that separates the two lines is 50 percent of the pen' s width, and the width of the second line is 30 percent of the pen's width. Start by creating a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object and an array of real numbers. You can then set the compound array by passing the array with the values 0.0, 0.2, 0.7, and 1.0 to the <b>Pen::SetCompoundArray</b> method of the 
				<b>Pen</b> object.

If you set the alignment of a 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw compound lines.


#### Examples



The following example creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object and sets the compound array for the pen. The code then draws a line using the 
						<b>Pen</b> object.


```cpp
VOID Example_SetCompoundArray(HDC hdc)
{
   Graphics graphics(hdc);

   // Create an array of real numbers and a Pen object.
   REAL compVals[6] = {0.0f, 0.2f, 0.5f, 0.7f, 0.9f, 1.0f};
   Pen pen(Color(255, 0, 0, 255), 30);

   // Set the compound array of the pen.
   pen.SetCompoundArray(compVals, 6);

   // Draw a line with the pen.
   graphics.DrawLine(&pen, 5, 20, 405, 200);
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcompoundarray">Pen::GetCompoundArray</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getcompoundarraycount">Pen::GetCompoundArrayCount</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>