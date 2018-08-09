---
UID: NF:gdiplusmatrix.Matrix.Reset
title: Matrix::Reset
author: windows-sdk-content
description: The Matrix::Reset method updates this matrix with the elements of the identity matrix.
old-location: gdiplus\_gdiplus_CLASS_Matrix_Reset_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\matrixclass\matrixmethods\reset_41.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Matrix class [GDI+],Reset method, Matrix.Reset, Matrix::Reset, Reset, Reset method [GDI+], Reset method [GDI+],Matrix class, _gdiplus_CLASS_Matrix_Reset_, gdiplus._gdiplus_CLASS_Matrix_Reset_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Matrix.Reset
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Matrix::Reset


## -description


The <b>Matrix::Reset</b> method updates this matrix with the elements of the identity matrix.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



The elements on the main diagonal of the identity matrix are 1. All other elements of the identity matrix are 0.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that represents a horizontal scaling by a factor of 5 and a vertical scaling by a factor of 3. The code calls the <b>Matrix::Reset</b> method to replace the elements of that matrix with the elements of the identity matrix. Then the code calls the 
						<a href="https://msdn.microsoft.com/c4ac476f-ee9d-439b-8686-3edfea64ec39">Matrix::Translate</a> method to update the matrix with the product of itself (the identity) and a translation matrix. The result is that the matrix represents only the translation, not the scaling. The code uses the matrix to set the world transformation of a 
						<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object and then draws a rectangle that is transformed according to that world transformation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Reset(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   Matrix matrix(5.0f, 0.0f, 0.0f, 3.0f, 0.0f, 0.0f);
   matrix.Reset();
   matrix.Translate(50.0f, 40.0f);

   graphics.SetTransform(&amp;matrix);
   graphics.DrawRectangle(&amp;pen, 0, 0, 100, 100);  
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9f744c2a-f1f3-4a7e-ab0c-37aa1df01623">Global and Local Transformations</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/9b62be8a-64fd-4e91-b38b-f05d911786f4">Matrix::IsIdentity</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

