---
UID: NF:gdipluspen.Pen.SetAlignment
title: Pen::SetAlignment (gdipluspen.h)

description: The Pen::SetAlignment method sets the alignment for this Pen object relative to the line.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetAlignment_penAlignment_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\setalignment.htm

ms.date: 12/05/2018
ms.keywords: Pen class [GDI+],SetAlignment method, Pen.SetAlignment, Pen::SetAlignment, SetAlignment, SetAlignment method [GDI+], SetAlignment method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetAlignment_penAlignment_, gdiplus._gdiplus_CLASS_Pen_SetAlignment_penAlignment_
ms.topic: method
f1_keywords: 
 - "gdipluspen/Pen.SetAlignment"
dev_langs:
 - c++
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
 - Pen.SetAlignment
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Pen::SetAlignment


## -description


The <b>Pen::SetAlignment</b> method sets the alignment for this 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object relative to the line.


## -parameters




### -param penAlignment [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a></b>

Element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a> enumeration that specifies the alignment setting of the pen relative to the line that is drawn. The default value is <b>PenAlignmentCenter</b>. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -remarks



If you set the alignment of a 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw compound lines or triangular dash caps.


#### Examples



The following example creates two 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a> objects and sets the alignment for one of the pens. The code then draws two lines using each of the pens.


```cpp
VOID Example_SetAlignment(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a black and a green pen.
   Pen blackPen(Color(255, 0, 0, 0), 1);
   Pen greenPen(Color(255, 0, 255, 0), 15);

   // Set the alignment of the green pen.
   greenPen.SetAlignment(PenAlignmentInset);

   // Draw two lines using each pen.
   graphics.DrawEllipse(&greenPen, 0, 0, 100, 200);
   graphics.DrawEllipse(&blackPen, 0, 0, 100, 200);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nl-gdipluspen-pen">Pen</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspen/nf-gdipluspen-pen-getalignment">Pen::GetAlignment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-penalignment">PenAlignment</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-pens-lines-and-rectangles-about">Pens, Lines, and Rectangles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-setting-pen-width-and-alignment-use">Setting Pen Width and Alignment</a>
 

 

