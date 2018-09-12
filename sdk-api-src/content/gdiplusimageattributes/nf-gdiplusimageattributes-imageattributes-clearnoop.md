---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearNoOp
title: ImageAttributes::ClearNoOp
author: windows-sdk-content
description: The ImageAttributes::ClearNoOp method clears the NoOp setting for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearNoOp_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearnoop.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
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
 - ImageAttributes.ClearNoOp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearNoOp


## -description


The <b>ImageAttributes::ClearNoOp</b> method clears the NoOp setting for a specified category. 


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the NoOp setting is cleared. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



You can disable color adjustment for a certain object type by calling the <a href="https://msdn.microsoft.com/en-us/library/ms535433(v=VS.85).aspx">ImageAttributes::SetNoOp</a> method. Later, you can reinstate color adjustment for that object type by calling the <b>ImageAttributes::ClearNoOp</b> method. For example, the following statement disables color adjustment for brushes:

<code>myImageAttributes.SetNoOp(ColorAdjustTypeBrush);</code>

The following statement reinstates the brush color adjustment that was in place before the call to <a href="https://msdn.microsoft.com/en-us/library/ms535433(v=VS.85).aspx">ImageAttributes::SetNoOp</a>:
				
				

<code>myImageAttributes.ClearNoOp(ColorAdjustTypeBrush);</code>


#### Examples

The following example creates an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object from a .emf file. The code also creates an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The <a href="https://msdn.microsoft.com/en-us/library/ms535431(v=VS.85).aspx">ImageAttributes::SetColorMatrix</a> call sets the brush color-adjustment matrix of that <b>ImageAttributes</b> object to a matrix that converts red to green. 

The code calls <a href="https://msdn.microsoft.com/en-us/library/ms536037(v=VS.85).aspx">DrawImage</a> three times, each time passing the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object and the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. When the image is drawn the first time, all the red painted by brushes is converted to green. (The red drawn by pens is not changed.) Before the image is drawn the second time, the code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535433(v=VS.85).aspx">ImageAttributes::SetNoOp</a> method of the <b>ImageAttributes</b> object. So when the image is drawn the second time, no color adjustment is applied to brushes. Before the image is drawn the third time, the code calls the <b>ImageAttributes::ClearNoOp</b> method, which reinstates the brush color-adjustment settings. So when the image is drawn the third time, all the red painted by brushes is converted to green.


```cpp

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
      &brushMatrix, 
      ColorMatrixFlagsDefault, 
      ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 0, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),        // source rect
      UnitPixel,
      &imAtt);

   // Temporarily disable brush color adjustment.
   imAtt.SetNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) without brush color adjustment.
   // There is no change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 80, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);

   // Reinstate brush color adjustment.
   imAtt.ClearNoOp(ColorAdjustTypeBrush);

   // Draw the image (metafile) using brush color adjustment.
   // Items filled with a brush change from red to green.
   graphics.DrawImage(
      &image,
      Rect(0, 160, image.GetWidth(), image.GetHeight()),  // dest rect
      0, 0, image.GetWidth(), image.GetHeight(),          // source rect
      UnitPixel,
      &imAtt);
}
				
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535427(v=VS.85).aspx">ImageAttributes::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535433(v=VS.85).aspx">ImageAttributes::SetNoOp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535438(v=VS.85).aspx">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

