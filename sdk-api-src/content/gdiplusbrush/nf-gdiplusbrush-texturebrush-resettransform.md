---
UID: NF:gdiplusbrush.TextureBrush.ResetTransform
title: TextureBrush::ResetTransform
author: windows-sdk-content
description: The TextureBrush::ResetTransform method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_ResetTransform_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\resettransform_13.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],ResetTransform method, TextureBrush.ResetTransform, TextureBrush::ResetTransform, _gdiplus_CLASS_TextureBrush_ResetTransform_, gdiplus._gdiplus_CLASS_TextureBrush_ResetTransform_
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
 - TextureBrush.ResetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# TextureBrush::ResetTransform


## -description


The <b>TextureBrush::ResetTransform</b> method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



Setting the transformation matrix to the identity matrix guarantees that no transformation is done. This method is often used to reset the transformation before making any adjustments (scaling, rotating, and so on) to it.


#### Examples



The following example creates a texture brush and sets the transformation of the brush. Next, the code uses the transformed brush to fill a rectangle. Then, the code resets the transformation of the brush and uses the untransformed brush to fill a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_ResetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a texture brush, and set its transformation.
   Image image(L"HouseAndTree.Gif");
   TextureBrush textureBrush(&amp;image);
   textureBrush.RotateTransform(30);

   // Fill a rectangle with the transformed texture brush.
   graphics.FillRectangle(&amp;textureBrush, 0, 0, 200, 100);

   textureBrush.ResetTransform();
   
   // Fill a rectangle with the texture brush (no transformation).
   graphics.FillRectangle(&amp;textureBrush, 250, 0, 200, 100);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/12e1e132-a93f-4438-8a1d-9036a43a8fd8">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/df4771b2-f3c0-41c3-b2a9-4eb460162f84">MatrixOrder</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/4fe7b87d-5568-4f1b-82b0-0edef2c7b296">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/514dd511-518a-42f1-86bc-c3270f82abee">TextureBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/b710bd0f-f1b2-4ab9-b7ef-d790c1f36a04">TextureBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/00df6637-afc5-411a-a724-ce5d6e0a64ec">TextureBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/ba1ecf7c-58ea-4832-b9b2-fce884180805">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/a414f0f5-0d75-420c-87ae-d83e0b7dfcd4">TextureBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

