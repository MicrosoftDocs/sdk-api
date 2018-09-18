---
UID: NF:gdiplusbrush.LinearGradientBrush.GetTransform
title: LinearGradientBrush::GetTransform
author: windows-sdk-content
description: The LinearGradientBrush::GetTransform method gets the transformation matrix of this linear gradient brush.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\gettransform_34matrix.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetTransform method, LinearGradientBrush.GetTransform, LinearGradientBrush::GetTransform, _gdiplus_CLASS_LinearGradientBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetTransform_matrix_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
 - LinearGradientBrush.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetTransform


## -description


The <b>LinearGradientBrush::GetTransform</b> method gets the transformation matrix of this linear gradient brush. 


## -parameters




### -param matrix [out]

Type: <b>Matrix*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object maintains a transformation matrix that can store any affine transformation. When you use a linear gradient brush to fill an area, GDI+ transforms the brush's boundary lines according to the brush's transformation matrix and then fills the area. The transformed boundaries exist only during rendering; the boundaries stored in the 
				<b>LinearGradientBrush</b> object are not transformed.


#### Examples



The following example creates a linear gradient brush and sets its transformation matrix. Next, the code gets the brush's transformation matrix and proceeds to inspect or use the matrix elements.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetTransform(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Construct a linear gradient brush, and set its transformation.
   LinearGradientBrush linGrBrush( 
      Point(0, 0),
      Point(200, 0),
      Color(255, 255, 0, 0),    // red
      Color(255, 0, 0, 255));   // blue

   Matrix matrixSet(0, 1, -1, 0, 0, 0);

   linGrBrush.SetTransform(&amp;matrixSet);

   // Obtain information about the linear gradient brush.
   Matrix matrixGet;
   REAL   elements[6];

   linGrBrush.GetTransform(&amp;matrixGet);
   matrixGet.GetElements(elements);  

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



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/366d5a91-6d0c-4352-8859-6a0e8ee081c3">LinearGradientBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

