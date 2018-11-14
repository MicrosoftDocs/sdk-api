---
UID: NF:gdiplusbrush.TextureBrush.SetTransform
title: TextureBrush::SetTransform
author: windows-sdk-content
description: The TextureBrush::SetTransform method sets the transformation matrix of this texture brush.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_SetTransform_matrix_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\settransform_41matrix.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SetTransform, SetTransform method [GDI+], SetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],SetTransform method, TextureBrush.SetTransform, TextureBrush::SetTransform, _gdiplus_CLASS_TextureBrush_SetTransform_matrix_, gdiplus._gdiplus_CLASS_TextureBrush_SetTransform_matrix_
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
 - TextureBrush.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusbrush.h
: 
- TextureBrush.SetTransform
: 
req.product: GDI+ 1.0
---

# TextureBrush::SetTransform


## -description


The <b>TextureBrush::SetTransform</b> method sets the transformation matrix of this texture brush.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the transformation matrix to use. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A 
				<b>TextureBrush</b> object maintains a transformation matrix that can store any affine transformation. When you use a texture brush to fill an area, Windows GDI+ transforms the brush's image according to the brush's transformation matrix and then fills the area. The transformed image exists only during rendering; the image stored in the 
				<b>TextureBrush</b> object is not transformed. For example, suppose you call  and then paint an area with <i>someTextureBrush.ScaleTransform(3)</i> and then paint an area with <i>someTextureBrush</i>. The width of the brush's image triples when the area is painted, but the image stored in <i>someTextureBrush</i> remains unchanged.


#### Examples



The following example creates a texture brush and sets the transformation of the brush. The code then uses the transformed brush to fill an ellipse.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_SetTransform(HDC hdc)
{
   Graphics graphics(hdc);

   Matrix matrix(2, 0, 0, 1, 0, 0);  // Horizontal stretch

   Image image(L"HouseAndTree.gif");
   TextureBrush textureBrush(&amp;image);
   textureBrush.SetTransform(&amp;matrix);
   graphics.FillEllipse(&amp;textureBrush, 0, 0, 400, 200); 
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/735a9b62-d913-4d06-83bf-86ae093a0dc1">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/12e1e132-a93f-4438-8a1d-9036a43a8fd8">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/4fe7b87d-5568-4f1b-82b0-0edef2c7b296">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/9843531d-7894-4d2f-b9da-b807ae307e4f">TextureBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

