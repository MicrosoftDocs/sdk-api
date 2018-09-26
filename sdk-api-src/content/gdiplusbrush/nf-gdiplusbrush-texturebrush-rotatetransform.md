---
UID: NF:gdiplusbrush.TextureBrush.RotateTransform
title: TextureBrush::RotateTransform
author: windows-sdk-content
description: The TextureBrush::RotateTransform method updates this texture brush's current transformation matrix with the product of itself and a rotation matrix.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\rotatetransform_9angle_order.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: RotateTransform, RotateTransform method [GDI+], RotateTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],RotateTransform method, TextureBrush.RotateTransform, TextureBrush::RotateTransform, _gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_, gdiplus._gdiplus_CLASS_TextureBrush_RotateTransform_angle_order_
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
 - TextureBrush.RotateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# TextureBrush::RotateTransform


## -description


The <b>TextureBrush::RotateTransform</b> method updates this texture brush's current transformation matrix with the product of itself and a rotation matrix.


## -parameters




### -param angle [in]

Type: <b>REAL</b>

Real number that specifies the angle, in degrees, of rotation. 


### -param order [in]

Type: <b><a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a> enumeration that specifies the order of the multiplication. <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a> specifies that the rotation matrix is on the left, and <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderAppend</a> specifies that the rotation matrix is on the right. The default value is <a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrderPrepend</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A single 3×3 matrix can store any sequence of affine transformations. If you have several 3×3 matrices, each of which represents an affine transformation, the product of those matrices is a single 3×3 matrix that represents the entire sequence of transformations. The transformation represented by that product is called a composite transformation. For example, suppose matrix R represents a rotation, and matrix T represents a translation. If matrix <i>M</i> is the product <i>RT</i>, then matrix <i>M</i> represents a composite transformation: first rotate, then translate.

The order of matrix multiplication is important. In general, the matrix product <i>RT</i> is not the same as the matrix product <i>TR</i>. In the example given in the previous paragraph, the composite transformation represented by <i>RT</i> (first rotate, then translate) is not the same as the composite transformation represented by <i>TR</i> (first translate, then rotate).


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill a rectangle.


```cpp
VOID Example_RotateTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&image);
   textureBrush.ScaleTransform(3, 1);                    // first scale
   textureBrush.RotateTransform(30, MatrixOrderAppend);  // then rotate
   graphics.FillRectangle(&textureBrush, 0, 0, 400, 200);
}
```





## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/62215ae0-b095-42b2-911c-aa7607a8b61a">Matrix Representation of Transformations</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/00df6637-afc5-411a-a724-ce5d6e0a64ec">TextureBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/ba1ecf7c-58ea-4832-b9b2-fce884180805">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/a414f0f5-0d75-420c-87ae-d83e0b7dfcd4">TextureBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

