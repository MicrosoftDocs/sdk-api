---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearColorMatrices
title: ImageAttributes::ClearColorMatrices
author: windows-sdk-content
description: The ImageAttributes::ClearColorMatrices method clears the color-adjustment matrix and the grayscale-adjustment matrix for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearColorMatrices_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearcolormatrices.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ClearColorMatrices, ClearColorMatrices method [GDI+], ClearColorMatrices method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearColorMatrices method, ImageAttributes.ClearColorMatrices, ImageAttributes::ClearColorMatrices, _gdiplus_CLASS_ImageAttributes_ClearColorMatrices_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorMatrices_type_
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
 - ImageAttributes.ClearColorMatrices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearColorMatrices


## -description


The <b>ImageAttributes::ClearColorMatrices</b> method clears the color-adjustment matrix and the grayscale-adjustment matrix for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the adjustment matrices are cleared. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a pair (color and grayscale) of adjustment matrices for the default category, a different pair of adjustment matrices for the bitmap category, and still a different pair of adjustment matrices for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a pair (color and grayscale) of adjustment matrices and a gamma value for the default category. If you set a pair of adjustment matrices for the pen category by calling <a href="https://msdn.microsoft.com/en-us/library/ms535430(v=VS.85).aspx">ImageAttributes::SetColorMatrices</a>, then the default adjustment matrices will not apply to pens. If you later clear the pen adjustment matrices by calling <b>ImageAttributes::ClearColorMatrices</b>, the pen category will not revert to the default adjustment matrices; rather, the pen category will have no adjustment matrices. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.


#### Examples



The following example creates an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object from a .emf file. The code also creates an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The first call to <a href="https://msdn.microsoft.com/en-us/library/ms535430(v=VS.85).aspx">ImageAttributes::SetColorMatrices</a> sets the default color-adjustment matrix and the default grayscale-adjustment matrix of the <b>ImageAttributes</b> object. The second call to <b>ImageAttributes::SetColorMatrices</b> sets the pen color-adjustment matrix and the pen grayscale-adjustment matrix of the <b>ImageAttributes</b> object. The four matrices perform as follows: 
						<ul>
<li>Default color: multiplies the red component by 1.5.</li>
<li>Default grayscale: multiplies the green component by 1.5.</li>
<li>Pen color: multiplies the blue component by 1.5.</li>
<li>Pen grayscale: multiplies red, green, and blue components by 1.5.</li>
</ul>


The code calls <a href="https://msdn.microsoft.com/en-us/library/ms536037(v=VS.85).aspx">DrawImage</a> once to draw the image with no color adjustment. Then the code calls <b>DrawImage</b> three more times, each time passing the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object and the address of the <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object. The second time the image is drawn (after the call that sets the default matrices), all the colors have their red components increased by 50 percent, and all the grays have their green components increased by 50 percent. The third time the image is drawn (after the call that sets the pen matrices), all the colors drawn by a pen have their blue components increased by 50 percent, and all the grays drawn by a pen have their red, green, and blue components increased by 50 percent. The fourth time the image is drawn (after the call to <b>ImageAttributes::ClearColorMatrices</b>), no adjustments are applied to colors and grays drawn by a pen.


```cpp

VOID Example_SetClearColorMatrices(HDC hdc)
{
   Graphics graphics(hdc);

   Image            image(L"TestMetafile6.emf");
   ImageAttributes  imAtt;
   RectF            rect;
   Unit             unit;

   image.GetBounds(&rect, &unit);

   ColorMatrix defaultColorMatrix = {  // Multiply red component by 1.5.
      1.5f,  0.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

   ColorMatrix defaultGrayMatrix = {  // Multiply green component by 1.5.
      1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  1.5f,  0.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  1.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

   ColorMatrix penColorMatrix = {     // Multiply blue component by 1.5.
      1.0f,  0.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  1.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  1.5f,  0.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

   ColorMatrix penGrayMatrix = {      // Multiply all components by 1.5.
      1.5f,  0.0f,  0.0f,  0.0f,  0.0f,
      0.0f,  1.5f,  0.0f,  0.0f,  0.0f,
      0.0f,  0.0f,  1.5f,  0.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  1.0f,  0.0f,
      0.0f,  0.0f,  0.0f,  0.0f,  1.0f};

   // Set the default color- and grayscale-adjustment matrices.
   imAtt.SetColorMatrices(
      &defaultColorMatrix,
      &defaultGrayMatrix, 
      ColorMatrixFlagsAltGray,
      ColorAdjustTypeDefault); 

   graphics.DrawImage(&image, 10.0f, 10.0f, rect.Width, rect.Height);

   graphics.DrawImage(
      &image, 
      RectF(10.0f, 50.0f, rect.Width, rect.Height),  // destination rectangle 
      rect.X, rect.Y,                // upper-left corner of source rectangle 
      rect.Width,                    // width of source rectangle
      rect.Height,                   // height of source rectangle
      UnitPixel,
      &imAtt);

   // Set the pen color- and grayscale-adjustment matrices.
   imAtt.SetColorMatrices(
      &penColorMatrix,
      &penGrayMatrix, 
      ColorMatrixFlagsAltGray,
      ColorAdjustTypePen); 

   graphics.DrawImage(
      &image, 
      RectF(10.0f, 90.0f, rect.Width, rect.Height),  // destination rectangle 
      rect.X, rect.Y,                // upper-left corner of source rectangle 
      rect.Width,                    // width of source rectangle
      rect.Height,                   // height of source rectangle
      UnitPixel,
      &imAtt);

   imAtt.ClearColorMatrices(ColorAdjustTypePen);

   graphics.DrawImage(
      &image, 
      RectF(10.0f, 130.0f, rect.Width, rect.Height),  // destination rectangle 
      rect.X, rect.Y,                // upper-left corner of source rectangle 
      rect.Width,                    // width of source rectangle
      rect.Height,                   // height of source rectangle
      UnitPixel,
      &imAtt); 
}
				
```


The following illustration shows the output of the preceding code.

<img alt="Illustration showing four rows of four ellipses each; the ones drawn with a pen vary in color more than the filled ones" src="./images/imageattributesclearcolormatrices.png"/>

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535417(v=VS.85).aspx">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535430(v=VS.85).aspx">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535431(v=VS.85).aspx">ImageAttributes::SetColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535438(v=VS.85).aspx">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

