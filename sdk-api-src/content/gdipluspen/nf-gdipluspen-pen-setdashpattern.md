---
UID: NF:gdipluspen.Pen.SetDashPattern
title: Pen::SetDashPattern (gdipluspen.h)
description: The Pen::SetDashPattern method sets an array of custom dashes and spaces for this Pen object.
helpviewer_keywords: ["Pen class [GDI+]","SetDashPattern method","Pen.SetDashPattern","Pen::SetDashPattern","SetDashPattern","SetDashPattern method [GDI+]","SetDashPattern method [GDI+]","Pen class","_gdiplus_CLASS_Pen_SetDashPattern_dashArray_count_","gdiplus._gdiplus_CLASS_Pen_SetDashPattern_dashArray_count_"]
old-location: gdiplus\_gdiplus_CLASS_Pen_SetDashPattern_dashArray_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setdashpattern.htm
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetDashPattern method, Pen.SetDashPattern, Pen::SetDashPattern, SetDashPattern, SetDashPattern method [GDI+], SetDashPattern method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetDashPattern_dashArray_count_, gdiplus._gdiplus_CLASS_Pen_SetDashPattern_dashArray_count_
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
 - Pen::SetDashPattern
 - gdipluspen/Pen::SetDashPattern
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
 - Pen.SetDashPattern
---

# Pen::SetDashPattern


## -description

The <b>Pen::SetDashPattern</b> method sets an array of custom dashes and spaces for this 
			<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.

## -parameters

### -param dashArray [in]

Type: <b>const REAL*</b>

Pointer to an array of real numbers that specifies the length of the custom dashes and spaces. All elements in the array must be positive real numbers.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the 
					<i>dashArray</i> array. The integer must be greater than 0 and not greater than the total number of elements in the array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

This method will set the 
				<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-dashstyle">DashStyle</a> enumeration for this 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to <b>DashStyleCustom</b>. 

The elements in the 
				<i>dashArray</i> array set the length of each dash and space in the dash pattern. The first element sets the length of a dash, the second element sets the length of a space, the third element sets the length of a dash, and so forth.

The length of each dash and space in the dash pattern is the product of the element value in the array and the width of the 
				<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.


#### Examples



The following example creates an array of real numbers. The code then creates a 
						<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, sets the dash pattern based on the array, and then draws the custom dashed line.


```cpp
VOID Example_SetDashPattern(HDC hdc)
{
   Graphics graphics(hdc);

   // Create and set an array of real numbers.
   REAL dashVals[4] = {
      5.0f,   // dash length 5
      2.0f,   // space length 2
      15.0f,  // dash length 15
      4.0f};  // space length 4

   // Create a Pen object.
   Pen pen(Color(255, 0, 0, 0), 5);

   // Set the dash pattern for the custom dashed line.
   pen.SetDashPattern(dashVals, 4);

   // Draw the custom dashed line.
   graphics.DrawLine(&pen, 5, 20, 405, 200); 
}
```

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-drawing-a-custom-dashed-line-use">Drawing a Custom Dashed Line</a>



<a href="/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpattern">Pen::GetDashPattern</a>



<a href="/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getdashpatterncount">Pen::GetDashPatternCount</a>



<a href="/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>