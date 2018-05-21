---
UID: NF:gdiplusgraphics.Graphics.ResetTransform
title: Graphics::ResetTransform
author: windows-driver-content
description: The Graphics::ResetTransform method sets the world transformation matrix of this Graphics object to the identity matrix.
old-location: gdiplus\_gdiplus_CLASS_Graphics_ResetTransform_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\resettransform.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: Graphics class [GDI+],ResetTransform method, Graphics.ResetTransform, Graphics::ResetTransform, ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_ResetTransform_, gdiplus._gdiplus_CLASS_Graphics_ResetTransform_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.ResetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::ResetTransform


## -description


The <b>Graphics::ResetTransform</b> method sets the world transformation matrix of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to the identity matrix.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The identity matrix represents a transformation that does nothing. If the world transformation matrix of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object is the identity matrix, then no world transformation is applied to items drawn by that <b>Graphics</b> object.


#### Examples



The following example sets the world transformation of a <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object to a 45-degree rotation and then draws a rectangle. The code calls the <b>ResetTransform</b> method of the <b>Graphics</b> object and then draws a second rectangle. No rotation transformation is applied to the second rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ResetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Rotate the transformation and draw a rectangle.
   graphics.RotateTransform(45.0f);
   Pen blackPen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&amp;blackPen, 100, 0, 100, 50);

   // Reset the transformation to identity, and draw a second rectangle.
   graphics.ResetTransform();
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawRectangle(&amp;redPen, 110, 0, 100, 50);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/f5f1a7bb-4f17-4865-b26e-8672ae78c3a7">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/46f90c3e-ed70-40ba-a8e8-1b1d3276862d">Graphics::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/554cd11e-9b22-48c5-a823-bd29f879fba7">Graphics::RotateTransform</a>



<a href="https://msdn.microsoft.com/040bfd10-1a2b-4277-9d27-0919d9efe371">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/d9c29b36-8f21-4d0b-99c7-5e7d635ee1a1">Graphics::TransformPoints</a>



<a href="https://msdn.microsoft.com/99b51fb7-b1de-421f-9743-bf6a5ec758ef">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

