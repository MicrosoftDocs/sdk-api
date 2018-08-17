---
UID: NF:gdiplusbrush.TextureBrush.ScaleTransform
title: TextureBrush::ScaleTransform
author: windows-sdk-content
description: The TextureBrush::ScaleTransform method updates this texture brush's current transformation matrix with the product of itself and a scaling matrix.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\scaletransform_32sx_sy_order.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ScaleTransform, ScaleTransform method [GDI+], ScaleTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],ScaleTransform method, TextureBrush.ScaleTransform, TextureBrush::ScaleTransform, _gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_, gdiplus._gdiplus_CLASS_TextureBrush_ScaleTransform_sx_sy_order_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusbrush.h
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
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - TextureBrush.ScaleTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# TextureBrush::ScaleTransform


## -description


The <b>TextureBrush::ScaleTransform</b> method updates this texture brush's current transformation matrix with the product of itself and a scaling matrix.


## -parameters




### -param sx [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the x direction. 


### -param sy [in]

Type: <b>REAL</b>

Real number that specifies the amount to scale in the y direction. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the scaling matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the scaling matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A single 3×3 matrix can store any sequence of affine transformations. If you have several 3×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix <i>T</i> represents a translation, and matrix <i>S</i> represents a scaling. If matrix <i>M</i> is the product <i>TS</i>, then matrix <i>M</i> represents a composite transformation: first translate, then scale.

The order of matrix multiplication is important. In general, the matrix product <i>RT</i> is not the same as the matrix product <i>TR</i>. In the example given in the previous paragraph, the composite transformation represented by <i>RT</i> (first rotate, then translate) is not the same as the composite transformation represented by <i>TR</i> (first translate, then rotate).


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ScaleTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&amp;image);
   textureBrush.RotateTransform(30);                      // first rotate
   textureBrush.ScaleTransform(3, 1, MatrixOrderAppend);  // then scale
   graphics.FillRectangle(&amp;textureBrush, 0, 0, 400, 200);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/4fe7b87d-5568-4f1b-82b0-0edef2c7b296">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/514dd511-518a-42f1-86bc-c3270f82abee">TextureBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/b710bd0f-f1b2-4ab9-b7ef-d790c1f36a04">TextureBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/ba1ecf7c-58ea-4832-b9b2-fce884180805">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/a414f0f5-0d75-420c-87ae-d83e0b7dfcd4">TextureBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

