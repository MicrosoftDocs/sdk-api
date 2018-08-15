---
UID: NF:gdiplusbrush.TextureBrush.ResetTransform
title: TextureBrush::ResetTransform
author: windows-sdk-content
description: The TextureBrush::ResetTransform method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_ResetTransform_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushmethods\resettransform_13.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ResetTransform, ResetTransform method [GDI+], ResetTransform method [GDI+],TextureBrush class, TextureBrush class [GDI+],ResetTransform method, TextureBrush.ResetTransform, TextureBrush::ResetTransform, _gdiplus_CLASS_TextureBrush_ResetTransform_, gdiplus._gdiplus_CLASS_TextureBrush_ResetTransform_
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
 - TextureBrush.ResetTransform
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# TextureBrush::ResetTransform


## -description


The <b>TextureBrush::ResetTransform</b> method resets the transformation matrix of this texture brush to the identity matrix. This means that no transformation takes place.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the 
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




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536332(v=VS.85).aspx">Coordinate Systems and Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533858(v=VS.85).aspx">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534526(v=VS.85).aspx">TextureBrush::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534530(v=VS.85).aspx">TextureBrush::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534534(v=VS.85).aspx">TextureBrush::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534536(v=VS.85).aspx">TextureBrush::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534538(v=VS.85).aspx">TextureBrush::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534542(v=VS.85).aspx">TextureBrush::TranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>
 

 

