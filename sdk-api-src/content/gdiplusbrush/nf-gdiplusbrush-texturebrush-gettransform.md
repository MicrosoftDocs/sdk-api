---
UID: NF:gdiplusbrush.TextureBrush.GetTransform
title: TextureBrush::GetTransform
author: windows-sdk-content
description: The TextureBrush::GetTransform method gets the transformation matrix of this texture brush.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_GetTransform_matrix_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\gettransform_92matrix.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetTransform, GetTransform method [GDI+], GetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],GetTransform method, TextureBrush.GetTransform, TextureBrush::GetTransform, _gdiplus_CLASS_TextureBrush_GetTransform_matrix_, gdiplus._gdiplus_CLASS_TextureBrush_GetTransform_matrix_
ms.prod: windows
ms.technology: windows-sdk
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
 - TextureBrush.GetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# TextureBrush::GetTransform


## -description


The <b>TextureBrush::GetTransform</b> method gets the transformation matrix of this texture brush.


## -parameters




### -param matrix [out]

Type: <b><a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that receives the transformation matrix. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A 
				<b>TextureBrush</b> object maintains a transformation matrix that can store any affine transformation. When you use a texture brush to fill an area, GDI+ transforms the brush's image according to the brush's transformation matrix and then fills the area. The transformed image exists only during rendering; the image stored in the 
				<b>TextureBrush</b> object is not transformed. For example, suppose you call <i>someTextureBrush.ScaleTransform(3)</i> and then paint an area with <i>someTextureBrush</i>. The width of the brush's image triples when the area is painted, but the image stored in <i>someTextureBrush</i> remains unchanged.


#### Examples




			The following example creates a texture brush and sets the transformation of the brush. The code then gets the brush's transformation matrix and proceeds to inspect or use the elements.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetTransform(HDC hdc)
{
   Graphics graphics(hdc);
  
   // Create a texture brush, and set its transform.
   Image image(L"marble.jpg");
   TextureBrush textureBrush(&amp;image);
   textureBrush.ScaleTransform(3, 2);

   // Obtain information about the texture brush.
   Matrix matrix;
   REAL elements[6];

   textureBrush.GetTransform(&amp;matrix);
   matrix.GetElements(elements);

   for(INT j = 0; j &lt;=5; ++j)
   {
      // Inspect or use the value in elements[j].
   }
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



<a href="https://msdn.microsoft.com/9843531d-7894-4d2f-b9da-b807ae307e4f">TextureBrush::ResetTransform</a>



<a href="https://msdn.microsoft.com/ba1ecf7c-58ea-4832-b9b2-fce884180805">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/4acf3d70-f119-4a5b-a20d-8adea453556f">Transformations</a>
 

 

