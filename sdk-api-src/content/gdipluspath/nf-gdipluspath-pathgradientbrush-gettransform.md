---
UID: NF:gdipluspath.PathGradientBrush.GetTransform
title: PathGradientBrush::GetTransform
author: windows-sdk-content
description: The PathGradientBrush::GetTransform method gets transformation matrix of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\gettransform_69matrix.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetTransform method, PathGradientBrush.GetTransform, PathGradientBrush::GetTransform, _gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetTransform_matrix_
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
 - PathGradientBrush.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetTransform


## -description


The <b>PathGradientBrush::GetTransform</b> method gets transformation matrix of this path gradient brush.


## -parameters




### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> object maintains a transformation matrix that can store any affine transformation. When you use a path gradient brush to fill an area, GDI+ transforms the brush's boundary path according to the brush's transformation matrix and then fills the interior of the transformed path. The transformed path exists only during rendering; the boundary path stored in 
						<b>PathGradientBrush</b>object is not transformed.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>object based on an array of three points. The 
						<a href="https://msdn.microsoft.com/en-us/library/ms535081(v=VS.85).aspx">PathGradientBrush::ScaleTransform</a> and 
						<a href="https://msdn.microsoft.com/en-us/library/ms535093(v=VS.85).aspx">PathGradientBrush::TranslateTransform</a> methods set the elements of the brush's transformation matrix so that the matrix represents a composite transformation (first scale, then translate). That composite transformation applies to the brush's boundary path, so the call to 
						<a href="https://msdn.microsoft.com/en-us/library/ms535957(v=VS.85).aspx">FillRectangle</a> fills the interior of a triangle that is the result of scaling and translating the boundary path. The code calls the <b>PathGradientBrush::GetTransform</b> method of the 
						<b>PathGradientBrush</b>object to obtain the brush's transformation matrix and then calls the 
						<a href="https://msdn.microsoft.com/en-us/library/ms535301(v=VS.85).aspx">GetElements</a> method of the retrieved <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object to fill an array with the matrix elements.

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




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536397(v=VS.85).aspx">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535091(v=VS.85).aspx">PathGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

