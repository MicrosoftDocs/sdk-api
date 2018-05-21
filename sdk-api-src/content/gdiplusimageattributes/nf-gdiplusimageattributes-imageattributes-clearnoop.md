---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearNoOp
title: ImageAttributes::ClearNoOp
author: windows-driver-content
description: The ImageAttributes::ClearNoOp method clears the NoOp setting for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearNoOp_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearnoop.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ClearNoOp, ClearNoOp method [GDI+], ClearNoOp method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearNoOp method, ImageAttributes.ClearNoOp, ImageAttributes::ClearNoOp, _gdiplus_CLASS_ImageAttributes_ClearNoOp_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearNoOp_type_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusimageattributes.h
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	ImageAttributes.ClearNoOp
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearNoOp


## -description


The <b>ImageAttributes::ClearNoOp</b> method clears the NoOp setting for a specified category. 


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the NoOp setting is cleared. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



You can disable color adjustment for a certain object type by calling the <a href="https://msdn.microsoft.com/bcb07aea-d700-4ba4-af2a-1870aedc67a7">ImageAttributes::SetNoOp</a> method. Later, you can reinstate color adjustment for that object type by calling the <b>ImageAttributes::ClearNoOp</b> method. For example, the following statement disables color adjustment for brushes:

<code>myImageAttributes.SetNoOp(ColorAdjustTypeBrush);</code>

The following statement reinstates the brush color adjustment that was in place before the call to <a href="https://msdn.microsoft.com/bcb07aea-d700-4ba4-af2a-1870aedc67a7">ImageAttributes::SetNoOp</a>:
				
				

<code>myImageAttributes.ClearNoOp(ColorAdjustTypeBrush);</code>


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object from a .emf file. The code also creates an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object. The <a href="https://msdn.microsoft.com/6fe73738-41f6-4ff3-bcd5-a885040bf48b">ImageAttributes::SetColorMatrix</a> call sets the brush color-adjustment matrix of that <b>ImageAttributes</b> object to a matrix that converts red to green. 

The code calls <a href="https://msdn.microsoft.com/ec2eb9c8-e5f1-4f0d-968f-e4ac16d670d6">DrawImage</a> three times, each time passing the address of the <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object and the address of the <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object. When the image is drawn the first time, all the red painted by brushes is converted to green. (The red drawn by pens is not changed.) Before the image is drawn the second time, the code calls the <a href="https://msdn.microsoft.com/bcb07aea-d700-4ba4-af2a-1870aedc67a7">ImageAttributes::SetNoOp</a> method of the <b>ImageAttributes</b> object. So when the image is drawn the second time, no color adjustment is applied to brushes. Before the image is drawn the third time, the code calls the <b>ImageAttributes::ClearNoOp</b> method, which reinstates the brush color-adjustment settings. So when the image is drawn the third time, all the red painted by brushes is converted to green.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID Example_SetClearNoOp(HDC hdc)
{
   Graphics graphics(hdc);

   Image image(L"TestMetafile4.emf");
   ImageAttributes imAtt;

    ColorMatrix brushMatrix = {     // red converted to green
      0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
      0.0f, 1.0f, 0.0f, 0.0f, 0.0f,
      0.0f, 0.0f, 1.0f, 0.0f, 0.0f,
      0.0f, 0.0f, 0.0f, 1.0f, 0.0f,
      0.0f, 0.0f, 0.0f, 0.0f, 1.0f};

   imAtt.SetColorMatrix(
      &amp;brushMatrix, 
      ColorMatrixFlagsDefault, 
      ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 0, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),        // source rect
      UnitPixel,
      &amp;imAtt);

   // Temporarily disable brush color adjustment.
   imAtt.SetNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) without brush color adjustment.
   // There is no change from red to green.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 80, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);

   // Reinstate brush color adjustment.
   imAtt.ClearNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &amp;image,
      Rect(0, 160, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &amp;imAtt);
}
				</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/27292b56-4bca-41bd-8923-b1d0e1a97c5e">ImageAttributes::Reset</a>



<a href="https://msdn.microsoft.com/bcb07aea-d700-4ba4-af2a-1870aedc67a7">ImageAttributes::SetNoOp</a>



<a href="https://msdn.microsoft.com/5b5f673b-f1f4-492e-b012-0c3b27abeeeb">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

