---
UID: NF:gdiplusgraphics.Graphics.TranslateTransform
title: Graphics::TranslateTransform
author: windows-sdk-content
description: The Graphics::TranslateTransform method updates this Graphics object's world transformation matrix with the product of itself and a translation matrix.
old-location: gdiplus\_gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\translatetransform.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Graphics class [GDI+],TranslateTransform method, Graphics.TranslateTransform, Graphics::TranslateTransform, TranslateTransform, TranslateTransform method [GDI+], TranslateTransform method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_, gdiplus._gdiplus_CLASS_Graphics_TranslateTransform_dx_dy_order_
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
 - Graphics.TranslateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::TranslateTransform


## -description


The <b>Graphics::TranslateTransform</b> method updates this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object's world transformation matrix with the product of itself and a translation matrix.


## -parameters




### -param dx [in]

Type: <b>REAL</b>

Real number that specifies the horizontal component of the translation. 


### -param dy [in]

Type: <b>REAL</b>

Real number that specifies the vertical component of the translation. 


### -param order [in, optional]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the translation matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the translation matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



<div class="alert"><b>Note</b>  GDI+ handles brushes differently when the world transform scale is less than 100%(1.0f) in either the x or y direction.  If the world transform scale is less than 100%(1.0f), be sure to multiply the offset for TranslateTransform by the world transform scale.</div>
<div> </div>

#### Examples



The following example sets the world transformation of a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object to a rotation. The call to <b>Graphics::TranslateTransform</b> multiplies the <b>Graphics</b> object's existing world transformation matrix (rotation) by a translation matrix. The MatrixOrderAppend argument specifies that the multiplication is done with the translation matrix on the right. At that point, the world transformation matrix of the <b>Graphics</b> object represents a composite transformation: first rotate, then translate. The call to <b>DrawEllipse</b> draws a rotated and translated ellipse.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_TranslateTransform(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   graphics.RotateTransform(30.0f);
   graphics.TranslateTransform(100.0f, 50.0f, MatrixOrderAppend);
   graphics.DrawEllipse(&amp;pen, 0, 0, 200, 80);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/f5f1a7bb-4f17-4865-b26e-8672ae78c3a7">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/10357224-cfbd-4d02-af94-93cdff80d466">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/040bfd10-1a2b-4277-9d27-0919d9efe371">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/d9c29b36-8f21-4d0b-99c7-5e7d635ee1a1">Graphics::TransformPoints</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

