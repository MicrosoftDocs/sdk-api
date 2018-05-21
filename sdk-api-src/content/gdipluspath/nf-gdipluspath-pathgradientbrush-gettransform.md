---
UID: NF:gdipluspath.PathGradientBrush.GetTransform
title: PathGradientBrush::GetTransform
author: windows-driver-content
description: The PathGradientBrush::GetTransform method gets transformation matrix of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\gettransform_69matrix.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetTransform method, PathGradientBrush.GetTransform, PathGradientBrush::GetTransform, _gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	PathGradientBrush.GetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetTransform


## -description


The <b>PathGradientBrush::GetTransform</b> method gets transformation matrix of this path gradient brush.


## -parameters




### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks




		A <a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a> object maintains a transformation matrix that can store any affine transformation. When you use a path gradient brush to fill an area, GDI+ transforms the brush's boundary path according to the brush's transformation matrix and then fills the interior of the transformed path. The transformed path exists only during rendering; the boundary path stored in 
						<b>PathGradientBrush</b>
 object is not transformed.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>
 object based on an array of three points. The 
						<a href="https://msdn.microsoft.com/085a33da-b9d6-4707-b368-200250b0823c">PathGradientBrush::ScaleTransform</a> and 
						<a href="https://msdn.microsoft.com/3e6d8b19-92a7-4e3c-983d-8f13e4a8f4ee">PathGradientBrush::TranslateTransform</a> methods set the elements of the brush's transformation matrix so that the matrix represents a composite transformation (first scale, then translate). That composite transformation applies to the brush's boundary path, so the call to 
						<a href="https://msdn.microsoft.com/eff3454e-f4d7-4cc2-9385-268d9ced2715">FillRectangle</a> fills the interior of a triangle that is the result of scaling and translating the boundary path. The code calls the <b>PathGradientBrush::GetTransform</b> method of the 
						<b>PathGradientBrush</b>
 object to obtain the brush's transformation matrix and then calls the 
						<a href="https://msdn.microsoft.com/8d0b7cb7-61cf-4a68-a843-9b68ac74a6b7">GetElements</a> method of the retrieved <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object to fill an array with the matrix elements.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetTransform(HDC hdc)
{
  Graphics graphics(hdc);

   // Create a path gradient brush and set its transformation.
   Point pts[] = {Point(0, 0), Point(50, 0), Point(50, 50)};
   PathGradientBrush pthGrBrush(pts, 3);
   pthGrBrush.ScaleTransform(3.0f, 1.0f);
   pthGrBrush.TranslateTransform(10.0f, 30.0f, MatrixOrderAppend);

   graphics.FillRectangle(&amp;pthGrBrush, 0, 0, 200, 200);

   // Obtain information about the path gradient brush.
   Matrix matrix;
   REAL elements[6];

   pthGrBrush.GetTransform(&amp;matrix);
   matrix.GetElements(elements);

   for(INT j = 0; j &lt;= 5; ++j)
   {
      // Inspect or use the value in elements[j].
   } 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/b31fe59b-33fb-4d8a-8b95-fd8b1ed78ac8">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

