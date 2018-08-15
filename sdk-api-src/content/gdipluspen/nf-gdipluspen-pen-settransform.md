---
UID: NF:gdipluspen.Pen.SetTransform
title: Pen::SetTransform
author: windows-sdk-content
description: The Pen::SetTransform method sets the world transformation of this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetTransform_matrix_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\settransform_6matrix.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Pen class [GDI+],SetTransform method, Pen.SetTransform, Pen::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_SetTransform_matrix_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspen.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Pen.SetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::SetTransform


## -description


The <b>Pen::SetTransform</b> method sets the world transformation of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the world transformation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



This method ignores the translation portion of the <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object.


#### Examples



The following example creates a scale matrix and a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object, and then draws a rectangle. The code then scales the pen by the matrix and draws a second rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Matrix matrix(20, 0, 0, 10, 0, 0);  // scale

   // Create a pen, and use it to draw a rectangle.
   Pen pen(Color(255, 0, 0, 255), 2);
   graphics.DrawRectangle(&amp;pen, 10, 50, 150, 100);

   // Scale the pen width by a factor of 20 in the horizontal 
   // direction and a factor of 10 in the vertical direction.
   pen.SetTransform(&amp;matrix);

   // Draw a rectangle with the transformed pen.
   graphics.DrawRectangle(&amp;pen, 200, 50, 150, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535035(v=VS.85).aspx">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535037(v=VS.85).aspx">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535038(v=VS.85).aspx">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535039(v=VS.85).aspx">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535040(v=VS.85).aspx">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

