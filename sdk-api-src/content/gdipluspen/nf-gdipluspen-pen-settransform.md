---
UID: NF:gdipluspen.Pen.SetTransform
title: Pen::SetTransform (gdipluspen.h)
author: windows-sdk-content
description: The Pen::SetTransform method sets the world transformation of this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\settransform_6matrix.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetTransform method, Pen.SetTransform, Pen::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_SetTransform_matrix_
ms.topic: method
f1_keywords: 
 - "gdipluspen/Pen.SetTransform"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetTransform
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::SetTransform


## -description


The <b>Pen::SetTransform</b> method sets the world transformation of this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object that specifies the world transformation. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



This method ignores the translation portion of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a> object.


#### Examples



The following example creates a scale matrix and a 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object, and then draws a rectangle. The code then scales the pen by the matrix and draws a second rectangle.


```cpp
VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Matrix matrix(20, 0, 0, 10, 0, 0);  // scale

   // Create a pen, and use it to draw a rectangle.
   Pen pen(Color(255, 0, 0, 255), 2);
   graphics.DrawRectangle(&pen, 10, 50, 150, 100);

   // Scale the pen width by a factor of 20 in the horizontal 
   // direction and a factor of 10 in the vertical direction.
   pen.SetTransform(&matrix);

   // Draw a rectangle with the transformed pen.
   graphics.DrawRectangle(&pen, 200, 50, 150, 100);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-coordinate-systems-and-transformations-about">Coordinate Systems and Transformations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix">Matrix</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-gettransform">Pen::GetTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-multiplytransform">Pen::MultiplyTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-resettransform">Pen::ResetTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-rotatetransform">Pen::RotateTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-scaletransform">Pen::ScaleTransform</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-transformations-use">Transformations</a>
 

 

