---
UID: NF:gdipluspen.Pen.SetTransform
title: Pen::SetTransform
author: windows-sdk-content
description: The Pen::SetTransform method sets the world transformation of this Pen object.
old-location: gdiplus\_gdiplus_CLASS_Pen_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\settransform_6matrix.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Pen class [GDI+],SetTransform method, Pen.SetTransform, Pen::SetTransform, SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_SetTransform_matrix_, gdiplus._gdiplus_CLASS_Pen_SetTransform_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Pen::SetTransform


## -description


The <b>Pen::SetTransform</b> method sets the world transformation of this 
			<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the world transformation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



This method ignores the translation portion of the <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object.


#### Examples



The following example creates a scale matrix and a 
						<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object, and then draws a rectangle. The code then scales the pen by the matrix and draws a second rectangle.

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




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/b62b1734-119a-4a65-854b-261674a02378">Pen::GetTransform</a>



<a href="https://msdn.microsoft.com/29ea3ff0-0cfa-4f4c-a292-824fdd0705ce">Pen::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/2a473f75-ad8c-4616-98fd-d87946409bb1">Pen::ResetTransform</a>



<a href="https://msdn.microsoft.com/c88b622c-3c9d-4640-96f5-0bccddd6f412">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/0605fcdb-bb04-46dd-8818-9d524a1d90d1">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

