---
UID: NF:gdiplusmatrix.Matrix.Invert
title: Matrix::Invert
author: windows-sdk-content
description: If this matrix is invertible, the Matrix::Invert method replaces the elements of this matrix with the elements of its inverse.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Invert_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\invert.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Invert, Invert method [GDI+], Invert method [GDI+],Matrix class, Matrix class [GDI+],Invert method, Matrix.Invert, Matrix::Invert, _gdiplus_CLASS_Matrix_Invert_, gdiplus._gdiplus_CLASS_Matrix_Invert_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusmatrix.h
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
 - Matrix.Invert
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Matrix::Invert


## -description


If this matrix is invertible, the <b>Matrix::Invert</b> method replaces the elements of this matrix with the elements of its inverse.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



If this matrix is not invertible, the method fails and returns InvalidParameter.


#### Examples



The following example passes the address of a 
						<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object to the 
						<a href="https://msdn.microsoft.com/458b62ad-04f0-4202-92db-b1fcf43b3ffa">SetTransform</a> method of a 
						<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object and then draws a rectangle. The rectangle is translated 30 units right and 20 units down by the world transformation of the 
						<b>Graphics</b> object. The code calls the <b>Matrix::Invert</b> method of the 
						<b>Matrix</b> object and sets the world transformation of the 
						<b>Graphics</b> object to the inverted matrix. The code draws a second rectangle that is translated 30 units left and 20 units up.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Invert(HDC hdc)
{
   Graphics myGraphics(hdc);
   Pen myPen(Color(255, 0, 0, 255));

   Matrix matrix(1.0f, 0.0f, 0.0f, 1.0f, 30.0f, 20.0f);

   myGraphics.SetTransform(&amp;matrix);
   myGraphics.DrawRectangle(&amp;myPen, 0, 0, 200, 100);
   matrix.Invert();
   myGraphics.SetTransform(&amp;matrix);
   myGraphics.DrawRectangle(&amp;myPen, 0, 0, 200, 100);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/7104f46b-3a3d-4185-9369-cfd89864de61">Matrix::IsInvertible</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

