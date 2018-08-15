---
UID: NF:gdipluspen.Pen.ResetTransform
title: Pen::ResetTransform
author: windows-sdk-content
description: The Pen::ResetTransform method sets the world transformation matrix of this Pen object to the identity matrix.
old-location: gdiplus\_gdiplus_CLASS_Pen_ResetTransform_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\penclass\penmethods\resettransform_27.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Pen class [GDI+],ResetTransform method, Pen.ResetTransform, Pen::ResetTransform, ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],Pen class, _gdiplus_CLASS_Pen_ResetTransform_, gdiplus._gdiplus_CLASS_Pen_ResetTransform_
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
 - Pen.ResetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Pen::ResetTransform


## -description


The <b>Pen::ResetTransform</b> method sets the world transformation matrix of this 
			<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object to the identity matrix.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<b>Ok</b> enumeration.




## -remarks



The identity matrix represents a transformation that does nothing. If the world transformation matrix of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object is the identity matrix, then no world transformation is applied to items drawn using that 
				<b>Pen</b> object.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534485(v=VS.85).aspx">Pen</a> object, sets a scaling matrix to the pen, and draws a rectangle. The code then resets the transformation of the pen and draws a second rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ResetTrans(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a pen, and set its transformation.
   Pen pen(Color(255, 0, 0, 255), 2);
   pen.ScaleTransform(8, 4);

   // Draw a rectangle with the transformed pen.
   graphics.DrawRectangle(&amp;pen, 50, 50, 150, 100);

   pen.ResetTransform();

   // Draw a rectangle with no pen transformation.
   graphics.DrawRectangle(&amp;pen, 250, 50, 150, 100);
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



<a href="https://msdn.microsoft.com/en-us/library/ms535039(v=VS.85).aspx">Pen::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535040(v=VS.85).aspx">Pen::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535056(v=VS.85).aspx">Pen::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

